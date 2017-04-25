# A Goal-Oriented Approach to Knowledge Discovery in Multi-Agent Systems

## Messages, Cooperation, and Sharing Knowledge

An agent is a knowledge-seeking system that stores and communicates information to/from a social environment, which is a network of communication lines that transmit signals between agents. If an agent does not recognize the information received, it sets a goal to obtain information that might lead to a clearer understanding.

Agents accomplish these information-seeking goals by reaching out to other agents for help. An agent might send a request to a neighbor, who may or may not have the desired information. If the recieving agent does not have the information, a request may be sent out to one of its own neighbors, and so on. This is called a 'request chain'.

Once the information is found, it is passed from agent-to-agent down the request chain, until the root agent receives the requested information. If the information is not found, or if the requested agent declines, the requester agent has the choice of whether or not to continue pursuing the goal. If the information is important, then there's a higher chance that the agent will continue sending requests to other agents, and therefore a higher chance that the goal is achieved.

## Goals, Competition, and Seeking Knowledge

An agent's goals revolve around knowledge discovery, meaning it is driven to obtain knowledge that it does not have. The payoff of any given action is equivalent to the predicted results of that action, with respect to the active set of goals. Therefore actions that result in new information being discovered will tend to have a higher payoff, especially when the new information matches that of a current goal. Current goals are selected based on the percieved importance of obtaining certain information.  

![Agent Structure](https://github.com/CarsonScott/Knowledge-Discovery-Agents/blob/master/newimage.png)

## Feedback, Conformity, and Seeking Approval

Agents send and recieve messages over time. The agents must adapt their ability to construct message in order to communicate information between one another. An agent’s drive toward knowledge discovery manifests initially as exploratory stochastic behavior and immediate feedback monitoring. 

Another drive that plays an important role at this stage is the power drive, which motivates the agent to exert control over its environment. This manifests as the desire for attention, which may be achieved by sending signals and observing feedback. The agent adaptively selects outputs that yield the highest amount of feedback from neighboring agents.

## Culture, Normalization, and Maintaining Order 

The system eventually conforms to a set of collectively-established behavioral norms. Conformity is essential to maintaining social order within a system because it exerts a suppressive force on individuals who behave in a way which deviates from social, political, or ideological standards of society. These individuals are labeled taboo and thus pose a threat to the wellbeing of others, or more importantly to the organization and stability of the current social system, namely the distribution of resources across various social classes within the population.

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

When an object is stored in the buffer, the semantic connections to other objects in the buffer are strengthened, resulting in higher semantic relevance between them. Semantic relevance refers to the geodesic distance between the nodes in the semantic net which correspond to stored objects in the buffer.

Output messages are constructed from available objects in the buffer. Objects are selected from the buffer and sent to the semantic network as input. This activates the nodes corresponding to the selected objects, and allows the activity to propagate to connected nodes throughout the network. Each new node that is activated is sent into the buffer. This is a technique that allows agents to 'seed' the available objects they can access, and consequently enabling objects to become active if they are related a currently active object. Another way of looking at it is terms of control. Without this technique, an agent has no control over the available objects from which the output messages are constructed. With the technique, the agent has more control, in that there is now an option available to replace a subset of objects in the buffer with other related objects.

Once the output message is constructed, objects contained in the message are stored back into the buffer, much like the concept of 'rehearsal' in psychology. Rehearsal occurs when an element of short-term memory is removed and then quickly placed back in as a new element, extending the amount of time it has until thee STM replaces it with a new object.

This is necessary for quick learning, because the STM's small capacity limits the amount of time that an object is allowed ti spend in STM.  Rehearsal provides a method of control, to some degree, over the memory system, since the agent manipulates the elapsed time of an object, as well as boosting the semantic relevance between the rehearsed object and the rest of STM.
