# Delivery example

The process consists of three lanes, namely,
one for customers, one for the order management, and one for the
delivery management.  In this process, the client first signs in and
then repeatedly looks for products.  Eventually, the client can decide
to give up (i.e., termination) or to make an order by submitting it to
the order management lane.  The client then waits for a response
(i.e., acceptance or refusal of this order).  However, the client
waits for a response for a maximum amount of time, what is represented
by a timer-event branch.  If the order can be completed, then the
parcel is received and the client pays for it.  Otherwise (i.e.,
timeout or order refused), the client fills in a feedback form.  As
far as the management lane is concerned, the first task aims at
verifying whether the goods ordered by the client are available.  If
they are not available, then the order is canceled; otherwise, the
order is confirmed.  The order management takes care of the payment of
the order whereas the delivery lane is triggered to prepare the parcel
to be delivered.  The delivery may be carried out by car or by drone.

There are several experiments you can reproduce just by loading the
files at the [delivery runs folder](./runs). To execute them, just cd
to that folder and load any of them into Maude.

~~~
runs$ maude bpmn-run-delivery-usage-10-25-1-0-5-2-70-80-60-1-0-4-2-70-80-50-1-0-3-2-70-80-40-1-0-2-2-70-80-20-1-0-3-2-70-80-30.maude
~~~

It will end up showing the resulting term with all the information of the simulation.
Find a summary of the results for these experiments in the [summary file](./runs/summary.txt).

![delivery process with legend and probabilities](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-legend-probs.png "delivery process with legend and probabilities")

<!-- referente to a file
[delivery process with legend and probabilities](../figs/delivery-legend-probs.png "")
to resize: | width=100
![delivery process with legend and probabilities](../figs/delivery-legend-probs.png | width=100)
-->

#### predictive-usage
TBC = 5, LAT = 10, POP = 1000,
clerk = [[1, 0], 5, [60, 90], 60],
worker = [[1, 0], 4, [60, 90], 50],
courier = [[1, 4], 3, [60, 90], 40],
car = [[1, 0], 2, [60, 90], 20],
drone = [[1, 4], 3, [60, 90], 30]

![delivery cars available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-car-type1.png "available instances" | width=100)
![delivery cars available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-car-type2.png "available instances")

![delivery clerks available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-clerk-type1.png "available instances")
![delivery clerks available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-clerk-type2.png "available instances")

![delivery couriers available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-courier-type1.png "available instances")
![delivery couriers available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-courier-type2.png "available instances")

![delivery drones available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-drone-type1.png "available instances")
![delivery drones available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-drone-type2.png "available instances")

![delivery workers available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-worker-type1.png "available instances")
![delivery workers available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-predictive-usage-5-5-10-1000-1-0-5-1-60-90--1--1-60-1-0-4-1-60-90--1--1-50-1-4-3-1-60-90--1--1-40-1-0-2-1-60-90--1--1-20-1-4-3-1-60-90--1--1-30-worker-type2.png "available instances")

#### usage
TBC = 10, CI = 10, POP = 1000,
clerk = [[1, 0], 5, [40, 80], 60],
worker = [[1, 0], 4, [40, 80], 50],
courier = [[1, 0], 3, [40, 80], 40],
car = [[1, 0], 2, [40, 80], 20],
drone = [[1, 0], 3, [40, 80], 30]

![delivery cars available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-car-type1.png "available instances")
![delivery cars available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-car-type2.png "available instances")

![delivery clerks available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-clerk-type1.png "available instances")
![delivery clerks available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-clerk-type2.png "available instances")

![delivery couriers available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-courier-type1.png "available instances")
![delivery couriers available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-courier-type2.png "available instances")

![delivery drones available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-drone-type1.png "available instances")
![delivery drones available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-drone-type2.png "available instances")

![delivery workers available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-worker-type1.png "available instances")
![delivery workers available instances](https://github.com/narudocap/maude-bpmn/blob/main/examples/delivery/figs/delivery-usage-10-10--1-1000-1-0-5-1-40-80--1--1-60-1-0-4-1-40-80--1--1-50-1-0-3-1-40-80--1--1-40-1-0-2-1-40-80--1--1-20-1-0-3-1-40-80--1--1-30-worker-type2.png "available instances")
