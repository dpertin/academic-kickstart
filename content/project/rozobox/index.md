---
title: "Rozobox: resilient distributed storage on 8 RPis"
date: 2014-06-01
draft: false

authors: ["Olivier Blin", "Quentin Lebourgeois", "Nicolas Normand",
          "Benoit Parrein", "Dimitri Pertin"]

summary: "Cluster of *Raspberry Pi*s to experiment, teach and popularize
          fault-tolerant distributed storage."

tags: ["Erasure code", "Mojette", "Polytech", "Université de Nantes"]

image:
  caption: "Cluster of 8 *Raspberry Pi*s v2! (v1 was based on a shoebox)"

links:
- name: Article (fr)
  url: http://web.polytech.univ-nantes.fr/actualites/lettre-d-informations/lettre-d-infos-n-17/la-rozobox-espace-de-stockage-made-in-polytech-nantes--1129345.kjsp

---

RozoBox is a cluster of 8 Raspberry Pis (RPis) used to experiment, teach and
popularize distributed storage. It was part of a project driven by two students
from Polytech Nantes: Olivier Blin and Quentin Lebourgeois, and supervised by
Nicolas Normand, and myself.

RozoFS was deployed on the RPis and leveraged their 8 SD cards to provide a
single storage volume that one can mount through the network.

To be fault-tolerant, RozoFS distributes redundant data across multiple servers.
To that end, when a movie is stored on RozoFS, it is split into multiple data
blocks. Each block is itself cut into data chunks, and some redundant chunks are
computed from them. For instance, to provide fault-tolerance against two
failures (like RAID-6), RozoFS computes two redundant chunks from four data
chunks (and we get 4+2 chunks). Then, each chunk is spread on different servers.
For reading, it is necessary to reach any subset of four chunks among the six
that were distributed during the write process.

To make things clearer, the students have developed a monitoring tool based on
*ncurses* which displayed the 8 RPis and enables give a quick statement of each
card regarding CPU/RAM/disk/network metrics and according to colors:
1. green: available (through the network) and idle;
2. yellow: available and working (read/write activity);
3. red: unavailable.

Thus, the demo was the following. I mounted the RozoFS volume from my computer
after plugging it to the network switch. Then I played a video stored on RozoFS
and the monitoring tool showed that 4 cards turned from green to yellow, meaning
they were implied in the video playing. Then I caused a failure by disconnecting
one of those implied card from the network. The video continued to be played
while the monitoring tool showed one reading card turning red, and another one
turning from green to yellow, meaning a first set of redundant chunks are used.

