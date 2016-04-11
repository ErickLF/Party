# Party
This example shows a simple multi-agent system where an host sets a party to which a number of agents are invited. This is also a stress test for the platform as the number of agents, messages, and agent conversations is very high. 

>> HostAgent

Description:
Agent representing the host for a party, to which a user-controlled number of guests is invited. The sequence is as follows:
the user selects a number guests to attend the party from 0 to 1000, using the slider on the UI. When the party starts, the host creates N guest agents, each of which registers with the DF, and sends the host a message to say that they have arrived. When all the guests have arrived, the party starts. The host selects one guest at random, and tells them a rumour. The host then selects two other guests at random, and introduces them to each other. The party then proceeds as follows: each guest that is introduced to someone asks the host to introduce them to another guest (at random). If a guest has someone introduce themselves, and the guest knows the rumour, they tell the other guest. When a guest hears the rumour for the first time, they notify the host. When all the guests have heard the rumour, the party ends and the guests leave.
Note: to start the host agent, it must be named ‘host’. Thus:
java jade.Boot -gui host:examples.party.HostAgent()

>> GuestAgent

Description:
Agent representing the guest for a party.

