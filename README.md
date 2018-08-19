# principles
Some simple principles I believe in and practice everyday

1. Own your **infrastructure**
	- The console is not your friend
	- API keys in non production environments is acceptable, but never in prod (use iam and security groups)
	- Always have a plan for CI/CD and have complete knowledge about your CI/CD tools and infrastructure
	- Repeatable infrastructure is not a good to have, it's a requirement
2. Make your code **testable**
	- Unit tests are a must (code coverage utilities are good but can be misleading, use with caution)
	- Mock out all external dependencies within your test suite (wiremocks for services, local DynamoDB, h2 in-memory db etc)
	- Attempt test driven development **(tdd)**
3. Own the **testing** of the software you write
	- Do not write and throw over the wall for someone else to test
	- If there is an obvious test case, find a way to automate it
4. **Design** for the business domain, for the cloud and for scale
	- Shit (unexplained) happens (especially in the cloud) : expect it, design for it
	- Be wary of bottlenecks, in a daisy chained type system, a single bottleneck can result in slowing down your entire system
	- Decoupling through fire and forget type systems are good, but require additional handling guarantees on the client side (idempotentcy etc)
	- Let the business needs and questions drive your design decisions i.e. design decisions must have rational rooted in a business need
	- Design for what you know first, be extra careful when designing for "in anticipation of" and "what if" scenarios
5. **Measurements** and **metrics**: Data driven decision making
	- Service level, function level
	- Business function level
	- Monitoring and logging
	- Its easier to make an argument for "If you break my system, I will find out" vs "You will not be able to break my system"
6. **Asynchronous** non blocking wherever possible
7. Developer **productivity** is important
	- Use tools that increase developer productivity
	- Shorter feedback cycles = greater developer productivity
8. **Documentation** is real and it is required
	- Keep it as close to the code as possible
	- Repository README's must have business function description, setup, test, local run and deploy instructions
	- Supplement with wiki
	- Stale documentation is worse than no documentation : keep your documentation up-to-date (or if possible self generating/updating)
9. **Simplicity is good**
	- It is tougher to design systems with lesser complexity, embrace that challenge
10. **Trunk** based development : reduced scope, extremely short lived branches.
11. **Agile** is great, and can have a myriad of variations.
	- As a team draft a **"How we work"** document, adhere to it
	- **Stand-ups** : Walk the board, rotate the person running stand-ups (daily, weekly)
	- Always attempt to move tickets all to way to the end (right most), before picking up another body of work
	- **Story writing** is an art, not a science
		- Keep them as small as possible while also demonstrating the value of doing this work
		- Include acceptance criteria on the ticket, this will govern how a ticket transitions from the "Ready for release" to "Value delivered"
	- **Estimation** : with time we get better at it as a team
		- Try and plant a seed estimation from a previous sprint during estimation of new stories
	- Dedicate time to conduct a productive **Retrospective**, do not let it devolve into an hour of venting
	- **Pair**: It is a great way to reduce the bad aspects of code ownership ("That's not my code, it's his/her"), and a great way to spread knowledge among members of the team.
12. **Don't fear** failure, i.e. don't be afraid to break things.. Caveat: as long as you learn from from every such instance.
13. Boy scout rule, DRY, KISS, SRP
