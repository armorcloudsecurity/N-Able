# armor_NAble
Automation of Armor Cloud Security with N-Able N-Central.

We have just performed a proof of concept on behalf of our MSP customers with N-Able N-Central.

N-Able's main RMM tool is called N-Central.

We can plug our Armor installation scripts into N-Central.

N-Central has their own agent that gets installed on every Windows machine. N-Central then uses that agent for their automation platform to push automation rules down to the machines. We have taken our Armor installation script and plugged it into N-Central automation - so that for example, if an MSP has ten customers, the MSP can input the Armor License Key one time for each customer, and the automation task will automatically install the Armor Agent across all of those customers machines, using the correct license key. If a customer adds more machines to their environment along with the N-Central agent, the Armor Agent security tools will automatically be installed on those machines.

The holy grail is, N-Central will check to see if the Armor Core windows service is running, and if it has gone down or in a Failed state, N-Central will "self heal" the Armor Core service, in other words restart the Armor service. The status check can be configured to run at any interval, such as 3 times in an hour for example.

Up to now, we have not needed to use the Armor API. We are simply taking advantage of the automation tools
in N-Central.
