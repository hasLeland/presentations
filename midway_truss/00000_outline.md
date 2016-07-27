
Outline
=======

<!--
Maybe for another time, but, the Definition of Microservices

0. Understandable business logic
1. Repeated code (rpc, transport)
2. Repeated code for reporting and metrics
		- YOU HAVE TO HAVE BOTH for things to function, but you get #2 for free with a monolith implicitly, but it can't be forgotten without everything going to shit.
-->


1. Motivation: Currently microservices requires worrying about much more than business logic.
	1. Microservice benefits: understandability of component microservices, composability, scaleability
	2. Microservice downsides: code (and documentation), and orchestration overhead
		1. Code boilerplate directly facilitating business logic
		2. Repeated code for reporting/logging/metrics
	- What is a microservice?
		- "Any group of logic that can be understood by an engineer in one business day."
2. Approach
	1. Abstract away problem 1 & 2 (+ documentation) into one definition
	2. Generate microservice (and documentation) from definition
	3. You define the microservice with gRPC, let truss handle the boilerplate, docs, and updating for you!
3. Demo the thing
	1. Show definition file
	2. Run `truss` on definiton file
	3. Look at documentation - compare to definition
	4. Look at service handlers - compare to definition
	5. Implement handler and re-run `truss`
	6. Show off that the client communcation with server works
	7. Add a new rpc, remove an old rpc, regenerate and see that the documentation changed, a handler was added, a handler was removed, and all other handlers are untouched
4. Roadmap 
	1. Roadmap
		1. http transport templating
		2. logging + metrics templating
		3. repeated message field automated generation client logic
		4. api explorer generation
	2. Call to info 
		- How is logging + metrics done, so we can implement those in microservices
5. Discussion


Approach: We built truss to solve these problems.
OLD
Problem Statement: Boilerplate is repetitious. Updating boilerplate is error prone. Documentation quickly becomes stale.



