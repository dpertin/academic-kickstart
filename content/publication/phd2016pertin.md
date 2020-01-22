---
title: "Mojette Erasure Code for Distributed Storage"
date: 2016-04-22
draft: false

authors: ["Dimitri Pertin"]
# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
publication_types: ["0"]
publication: "Ph.D (manuscript in french, slides in english)"

abstract: "Erasure codes can generate data redundancy in distributed storage
systems. This redundancy can be used to recover missing data in case of a
failure. Codes have the benefit of reducing the generated amount of redundancy
drastically,compared to plain data replication. However, this reduction is
combined with a significant computational complexity, which penalizes encoding
and decoding performances, and limits the use of coding to cold data. In this
thesis, we focus on the use of the Mojette transform as an effective erasure
code, adapted to hot data. The resulting code requires more redundancy than
classical codes though. The first contribution of this research work deals with
the design of a systematic version of the Mojette erasure code. This version
provides better performances while reducing the required amount of redundancy.
The second contribution covers the integration of this solution in the
distributed file system RozoFS. This integration enables the system to provide
a continuous service despite failures, while being able to manage hot data with
half the volume of data compared to replication-based systems. A third research
focus addresses the design of a distributed method to compute extra Mojette
codeword symbols. This method contributes to restore a redundancy threshold in
the storage system."

projects: ["fec4cloud"]
url_hal: "https://hal.archives-ouvertes.fr/tel-01720038/document"
url_pdf: "https://hal.archives-ouvertes.fr/tel-01720038/document"
url_slides: "https://hal.archives-ouvertes.fr/tel-01720038/file/these.pdf"
url_code: "https://github.com/denaitre/phd"
---

