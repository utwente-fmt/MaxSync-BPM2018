# MaxSync-BPM2018
Maximizing Synchronization for Aligning Observed and Modelled Behaviour
===

This repository hosts the results for the paper.

Please note that all experiments in the paper were performed on an
Intel Core<sup>TM</sup> i7-4710MQ processor with 2.50GHz and 7.4Gib memory,
running Debian Stretch.

Submitted and accepted at [BPM 2018].

Authors:
---

* Formal Methods and Tools, University of Twente, The Netherlands
    - Vincent Bloemen*:      [<v.bloemen@utwente.nl>](mailto:v.bloemen@utwente.nl)
    - Jaco van de Pol:       [<j.c.vandepol@utwente.nl>](mailto:j.c.vandepol@utwente.nl)

* Eindhoven University of Technology, Eindhoven, The Netherlands
    - Sebastiaan van Zelst: [<s.j.v.zelst@tue.nl>](mailto:s.j.v.zelst@tue.nl)
    - Boudewijn van Dongen: [<b.f.v.dongen@tue.nl>](mailto:b.f.v.dongen@tue.nl)

* Process and Data Science, RWTH Aachen University, Germany
    - Wil van der Aalst: [<wvdaalst@pads.rwth-aachen.de>](mailto:wvdaalst@pads.rwth-aachen.de)

\* Supported by the 3TU.BSR project.

Abstract
---
*Conformance checking is a branch of process mining that aims to assess to what
degree event data originating from the execution of a (business) process and a
corresponding reference model conform to each other. Alignments have been
recently introduced as a solution for conformance checking and have since
rapidly developed into becoming the de facto standard.*

*The state-of-the-art method to compute alignments is based on solving a
shortest path problem derived from the reference model and the event
data. Within such a shortest path problem, a cost function is used to guide the
search to an optimal solution.  The standard cost-function treats mismatches in
the model and log as equal.  In this paper, we consider a variant of this
standard cost function which maximizes the number of correct matches instead.
We study the effects of using this cost-function compared to the standard cost
function on both small and large models using over a thousand generated and
industrial case studies.*

*We further show that the alignment computation process can be sped up
significantly in specific instances. Finally, we present a new algorithm for
the computation of alignments on models with many log traces that is an order
of magnitude faster (in maximizing synchronous moves) compared to the
state-of-the-art A&#42; based solution method, as a result of a preprocessing
step on the model.*


Implementation
---

The implementation for A&#42; and the transitive closure graph algorithm are
available in [ProM] 6.8 toolset (the transitive closure graph algorithm is
implemented in the `MaxSyncAlignments` package). 

The source code for the Symbolic alignment algorithm is obtained by the
following command:
* `$ git clone git@github.com:vbloemen/ltsmin.git -b acsd18 --recursive`

If you experience any issues with the installation please consult the [LTSmin] 
website for further instructions. Otherwise, or if you would like help to
repeat the experiments please contact the first author ([Vincent
Bloemen](mailto:v.bloemen@utwente.nl)) for further help.

Data
---

The data used in this paper is currently being uploaded to the 4TU data centre,
the corresponding DOI will be placed here when it is done. Meanwhile, you
can contact the first author ([Vincent Bloemen](mailto:v.bloemen@utwente.nl))
if you would like to obtain the data.

[ProM]: http://www.promtools.org/doku.php
[LTSmin]: http://fmt.cs.utwente.nl/tools/ltsmin/
[BPM 2018]: http://bpm2018.web.cse.unsw.edu.au/index.html








