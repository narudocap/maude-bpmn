# Maude-based analaysis of BPMN processes

This repository contains information, code and examples related to the Maude specification of BPMN processes.

Business process verification and optimization is a strategic activity in organizations
because of its potential to increase profit margins and reduce
operational costs. One of the main challenges in this activity is
concerned with the problem of optimizing allocation and sharing of
resources.  Companies are continuously adjusting their resources to their needs
following different strategies.

Our latest efforts are related to the analysis of dynamic provisioning.
This repo provides info on an automatic analysis technique to
evaluate and compare the execution time and resource occupancy of a business
process relative to a workload and a provisioning strategy.
Four different strategies are considered, which are guided, respectively,
by the recent resource usage, by the recent resource request, by its
predicted behavior, and by a combination of available strategies.

Such analysis is performed on models conforming to an extension of BPMN with
quantitative information, including resource availability and constraints.
Within this framework, the approach is fully mechanized using a formal and
executable specification in the rewriting logic framework, which relies on
existing techniques and tools for simulating probabilistic and real-time
specifications.

This site contains the Maude specification and information related to several examples.

The structure of the repo is as follows:

- `/src` contains the main files of the Maude specification.
  - `bpmn.maude` contains the definitions for the representation of the BPMN
      process and the rules describing the BPMN behavioral semantics.
  - `bpmn-analysis.maude`	contains operations for the automated analysis of BPMN processes.
  - `supervisor-queues.maude`, `supervisor-usage-queues.maude`, `supervisor-predictive-usage.maude`, and `supervisor-usage.maude` contain the specification of the different strategies.
  - `bpmn-prelude.maude`, `my-real-time-maude.maude`, and `mgDistributions.maude`	contain some auxiliry machinery.
- `/examples` contains files related to the analysis of several example BPMN processes.
  - `/examples/delivery`
  - `/examples/recruitment`

Each of the example folders contains the corresponding specification, graphical representations of the processes (`figs/`) and sample experiments (`runs/`).
You can find information on how to execute the examples in their respective README files.

The paper includes results on the extensive experimentation that has been
carried out.

Several papers have been published on different contributions related to this project:
- F. Durán, C. Rocha, and G. Salaün:
[Analysis of the Runtime Resource Provisioning of BPMN Processes Using Maude](https://doi.org/10.1007/978-3-030-63595-4_3).
In S. Escobar and N. Martí-Oliet (eds.),
13th International Workshop Rewriting Logic and Its Applications (WRLA), Lecture Notes in Computer Science 12328, Springer, 2020.
- F. Durán, C. Rocha, and G. Salaün:
[A rewriting logic approach to resource allocation analysis in business process models](https://doi.org/10.1016/j.scico.2019.102303). Sci. Comput. Program. 183, 2019.
- F. Durán, C. Rocha, and G. Salaün:
[Analysis of Resource Allocation of BPMN Processes](https://doi.org/10.1007/978-3-030-33702-5_35).
In S. Yangui, I. Bouassida Rodriguez, K. Drira, and Z. Tari (eds.),
17th International Conference on Service-Oriented Computing (ICSOC), Lecture Notes in Computer Science 11895, pages 452-457, Springer, 2019.
- F. Durán, C. Rocha, and G. Salaün:
[Stochastic analysis of BPMN with time in rewriting logic](https://doi.org/10.1016/j.scico.2018.08.007). Sci. Comput. Program. 168: 1-17, 2018.
- F. Durán, C. Rocha, and G. Salaün:
[Computing the Parallelism Degree of Timed BPMN Processes](https://doi.org/10.1007/978-3-030-04771-9_24).
In 	M. Mazzara, I. Ober, and G. Salaün (eds.),
STAF 2018 Collocated Workshops, Lecture Notes in Computer Science 11176, pages 320-335, Springer, 2018.
- F. Durán, C. Rocha, and G. Salaün: [Symbolic Specification and Verification of Data-Aware BPMN Processes Using Rewriting Modulo SMT](https://doi.org/10.1007/978-3-319-99840-4_5). In V. Rusu (ed.): 12th International Workshop on Rewriting Logic and Its Applications (WRLA), Lecture Notes in Computer Science 11152, pages 76-97, Springer, 2018.
- F. Durán and G. Salaün: [Verifying Timed BPMN Processes Using Maude](https://doi.org/10.1007/978-3-319-59746-1_12). In J.-M. Jacquet and M. Massink (eds.), 19th IFIP WG 6.1 International Conference on Coordination Models and Languages (COORDINATION), Lecture Notes in Computer Science 10319, pages 219-236, Springer, 2017.

There are two companion sites where info on previous contributions of our project on the analysis of BPMN processes can be found:
- In http://maude.lcc.uma.es/BPMN-P/ there are tools for the analysis of
the maximum/minimum/average execution time and the timed degree of parallelism of simple BPMN processes.
- In http://maude.lcc.uma.es/BPMN-R/ first steps towards the analysis of resource allocation are documented.
