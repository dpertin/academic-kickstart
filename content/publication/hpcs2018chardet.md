---
title: "Madeus: a Formal Deployment Model"
date: 2018-07-16
draft: false

authors: ["Maverick Chardet", "Hélène Coullon", "Dimitri Pertin",
          "Christian Pérez"]

publication_types: ["1"]
publication: "In Proceedings of the International Conference on High Performance
              Computing Simulation (HPCS)"
publication_short: "HPCS"

abstract: "Distributed software architectures are composed of multiple interacting
modules, or components. Deploying such software consists in installing them on a
given infrastructure and leading them to a functional state. However, since each
module has its own life cycle and might have various dependencies with other
modules, deploying such software is a very tedious task, particularly on
massively distributed and heterogeneous infrastructures. To address this
problem, many solutions have been designed to automate the deployment process.
In this paper, we introduce Madeus, a component-based deployment model for
complex distributed software. Madeus accurately describes the life cycle of each
component by a Petri net structure, and is able to finely express the
dependencies between components. The overall dependency graph it produces is
then used to reduce deployment time by parallelizing deployment actions. While
this increases the precision and performance of the model, it also increases its
complexity. For this reason, the operational semantics needs to be clearly
defined to prove results such as the termination of a deployment. In this paper,
we formally describe the operational semantics of Madeus, and show how it can be
used in a use- case: the deployment of a real and large distributed software
(i.e., OpenStack)."

projects: ["Madeus"]
url_hal: "https://hal.inria.fr/hal-01858150"
url_pdf: "https://hal.inria.fr/hal-01858150/document"
---

