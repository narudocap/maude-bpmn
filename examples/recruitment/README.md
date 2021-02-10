# Recruitment example

Candidates fill up requested
forms, have a medical check-up, and, if necessary, apply for a visa.
Then, they submit the required documents.  If rejected, they can
re-apply.  Minor problems on the presented documentation may be
amended by submitting additional documentation.  The presented
documentation is checked by human resources (HR) officers, who decide
to either reject, accept or partially accept the presented
documentation.  If accepted, either through a direct accept or after
completing the pending documentation, some wages are anticipated, a
welcome kit is prepared, and the corresponding information in the
company's DB are updated.  Regarding resources, all tasks related to
documentation checking and wages anticipation are carried out by HR
officers, welcome kits are prepared by assistants, and DB updates are
carried out by technical staff (IT technicians).

There are several experiments you can reproduce just by loading the
files at the [recruitment/runs folder](./runs). To execute them, just cd
to that folder and load any of them into Maude.

~~~
runs$ maude bpmn-run-recruitment-usage-10-25-1-0-10-2-60-80-90-1-0-2-2-60-80-50-1-0-5-2-60-80-70.maude
~~~

It will end up showing the resulting term with all the information of the simulation.

<!-- embedded in text
![delivery process with legend and probabilities](../figs/delivery-legend-probs.png "delivery process with legend and probabilities")

<!-- referente to a file
[delivery process with legend and probabilities](../figs/delivery-legend-probs.png "")
to resize: | width=100
![delivery process with legend and probabilities](../figs/delivery-legend-probs.png | width=100)

delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-car-type1.png
delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-car-type2.png
delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-clerk-type1.png
delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-clerk-type2.png
delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-courier-type1.png
delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-courier-type2.png
delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-drone-type1.png
delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-drone-type2.png
delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-worker-type1.png
delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-worker-type2.png
delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-car-type1.png
delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-car-type2.png
delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-clerk-type1.png
delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-clerk-type2.png
delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-courier-type1.png
delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-courier-type2.png
delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-drone-type1.png
delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-drone-type2.png
delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-worker-type1.png
delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-worker-type2.png
-->
