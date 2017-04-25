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

## Memory, Communication, and Extracting Messages

An agent has a knowledge base called memory that stores information which can be accessed using keywords. Each element of memory contains a keyword and a value. A keyword acts as a label for tithe associated value in memory. 

An agent observes a stream of characters over time. Certain combinations of characters are recognized as messages. A message describes an action that the agent may or may not choose to perform. Messages contain an operator symbol, along with either two keywords or one keyword and one value. A message is an operation that manipulates the data in an agent’s memory. Each message has a type that is signified by the operator. Statements are messages that alter the stored values in memory. The possible types of statements are as follows:

1)	Definition
2)	Addition
3)	Subtraction
4)	Multiplication
5)	Division
6)	Exponent 

Questions are messages that retrieve information about the stored values in memory. The possible types of questions are as follows:

7)	What Is
8)	Is
9)	Is Not
10)	Is Above
11)	Is Below

Messages must be extracted from streaming input, where a single character is received at each time step. An agent constructs a message, or set of strings containing the individual components of a message, from the streaming input. Example:

Input:	      ‘x=5;’

Message:    ['x', '=', '5']

A message is constructed by searching for 'indicators', or symbols that trigger certain state-transitions, depending on the current state. The initial state is -1, meaning no message is currently being constructed. Once any characters are received, the state becomes 0. 

Characters received in 0 are stored in the first element of the message, until the input character matches an operator symbol. This is an indicator that triggers the current state to change from 0 to 1.  Characters received in 1 are stored in the second element of the message, until a non-operator symbol is received. This triggers the state to change from 1 to 2. Characters received in 2 are stored in the second element of the message, until a stop symbol (;) is received. The agent exits the construction stage and begins the execution stage. If the message is valid, a set of outputs (if any) is returned, and the keywords contained in the message are stored in a buffer, which is a finite set of recently active keywords analogous to short-term memory.

## Output, Rehearsal, and Constructing Messages

When an object is stored in the buffer, semantic connections between themselves and the other objects in the buffer are strengthened, resulting in greater semantic relevance between them. Semantic relevance refers to the geodesic distance between the nodes in a semantic net that correspond to stored objects in the buffer.

Output messages are constructed from available objects in the buffer. Objects are selected from the buffer and removed, and the semantic net receives an input which activates the nodes corresponding to the selected objects. The inputs propagate from node-to-node across semantic connections, and the set of nodes that become active are stored in the buffer. Essentially, this process is a seeding function, which allows access to knowledge that has not been activated by external stimuli.

Once the output message is constructed and sent, the objects contained in the message are sent back to the buffer, which is very similar to the psychological concept of rehearsal. Rehearsal occurs when an element of short-term memory is removed and then quickly placed back in as a new element. 

This is necessary for quicker learning in spite of the STM’s limited capacity. When an object is rehearsed, the elapsed time since it was stored in the STM resets, extending the object’s total time in STM, and therefore strengthening the connections in the semantic net between the rehearsed object and every other stored object in the STM.
