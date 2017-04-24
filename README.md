# A Goal-Oriented Approach to Knowledge Discovery in Multi-Agent Systems

## Messages, Cooperation, and Sharing Knowledge

An agent is a knowledge-seeking system that stores and communicates information to/from a social environment, which is a network of communication lines that transmit signals between agents. If an agent does not recognize the information received, it sets a goal to obtain information that might lead to a clearer understanding.

Agents accomplish these information-seeking goals by reaching out to other agents for help. An agent might send a request to a neighbor, who may or may not have the desired information. If the recieving agent does not have the information, a request may be sent out to one of its own neighbors, and so on. This is called a 'request chain'.

Once the information is found, it is passed from agent-to-agent down the request chain, until the root agent receives the requested information. If the information is not found, or if the requested agent declines, the requester agent has the choice of whether or not to continue pursuing the goal. If the information is important, then there's a higher chance that the agent will continue sending requests to other agents, and therefore a higher chance that the goal is achieved.

## Goals, Competition, and Seeking Knowledge

An agent's goals revolve around knowledge discovery, meaning it is driven to obtain knowledge that it does not have. The payoff of any given action is equivalent to the predicted results of that action, with respect to the active set of goals. Therefore actions that result in new information being discovered will tend to have a higher payoff, especially when the new information matches that of a current goal. Current goals are selected based on the percieved importance of obtaining certain information.  

![](https://github.com/CarsonScott/Knowledge-Discovery-Agents/blob/master/Activity%20Diagram3.png)

## Feedback, Conformity, and Seeking Approval

Agents send and recieve messages over time. The agents must adapt their ability to construct message in order to communicate information between one another. An agent’s drive toward knowledge discovery manifests initially as exploratory stochastic behavior and immediate feedback monitoring. 

Another drive that plays an important role at this stage is the power drive, which motivates the agent to exert control over its environment. This manifests as the desire for attention, which may be achieved by sending signals and observing feedback. The agent adaptively selects outputs that yield the highest amount of feedback from neighboring agents.

## Culture, Normalization, and Maintaining Order 

Specific input patterns can cause internal events to trigger within another agent. For example, the language-building system used to construct sentences may be triggered externally by another agent, whose signal patterns activate the receiving agent’s language system. An agent’s resistance to external signals is very weak at the initial stage but over time becomes stronger, resulting in an agent who’s highly self-driven and less influenced by the environment.

The system eventually conforms to a set of collectively-established behavioral norms. Conformity is essential to maintaining order within social systems. Conformity exerts a suppressive force on individuals that behave in a way that deviates from the social, political, or ideological standards of the society. These “taboo” individuals may pose a threat to the population itself, or it may pose a threat to the current stability/organization of the societal system, for instance the distribution of resources across various social classes within the population.
