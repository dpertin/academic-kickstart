---
title: "A Distributed File System Based on Erasure Coding for I/O-Intensive
Applications"
date: 2014-04-03
draft: false

authors: ["Dimitri Pertin", "Sylvain David", "Pierre Evenou",
"Benoît Parrein", "Nicolas Normand"]

publication_types: ["1"]
publication: "In Proceedings of the 4th International Conference on Cloud
Computing and Service Science"
publication_short: "CLOSER"

abstract: "Distributed storage systems take advantage of the network, storage
and computational resources to provide a scalable infrastructure. But in such
large system, failures are frequent and expected. Data replication is the
common technique to provide fault-tolerance but suffers from its important
storage consumption. Erasure coding is an alternative that offers the same
data protection but reduces significantly the storage consumption. As it
entails additional workload, current storage providers limit its use for
longterm storage. We present the Mojette Transform (MT), an erasure code whose
computations rely on fast XOR operations. The MT is part of RozoFS, a
distributed file system that provides a global namespace relying on a cluster
of storage nodes.
This work is part of our ongoing effort to prove that erasure coding is not
necessarily a bottleneck for intense I/O applications. In order to validate our
approach, we consider a case study involving a storage cluster of RozoFS that
supports video editing as an I/O intensive application."

projects: ["fec4cloud"]
url_hal: "https://hal.archives-ouvertes.fr/hal-01149847"
url_pdf: "https://hal.archives-ouvertes.fr/hal-01149847/document"
---

