1. Title

  Multi-project GitHub Search and Advanced Concurrent Repository Exploration in Go

2. Elevator Pitch (300 characters)

  When creating a tool in Go for advanced GitHub search and concurrent repository
  exploration, we encountered many challenges. In addition to highlighting how
  community standards support language and package discovery, this talk explains
  the design decisions that we made to support concurrency.

3. Audience Level (Beginner? Intermediate?)

  Beginner

4. Description (seen by attendees)

  When creating a tool for advanced GitHub search and concurrent repository
  exploration, we encountered challenges with language choice, package discovery
  and designing a tool with support for concurrency. The Go community offers a
  clear standard going for dependency management and centralized resource for
  package discovery and documentation with modules and GoDoc, respectively.
  In addition to the aforementioned offerings, the Go community has well-defined
  patterns for concurrency. While highlighting the reasons for choosing to write
  our tool in Go, this talk provides justification for supporting concurrency
  using a fanout design pattern, the steps for identifying and fixing race
  conditions and trade-offs between unbuffered and buffered channels.

5. Notes (only be seen by reviewers during the CFP process. This is where you
   should explain things such as technical requirements, why you're the best
   person to speak on this subject, etc.)

  In this talk I will discuss the challenges faced and lessons learned while creating
  my first personal open source tool in Go. This project helped identify the importance of
  community and clearly-defined standards. From both a negative and positive perspective
  with the numerous competing standards for dependency management with no clear
  "leader" in Python and the clearly-defined pipeline techniques in Go, respectively.
  Additionally, at StockX, I have designed and implemented a few systems that use a
  similar design to that of neighbor, namely the fanout design.

  Having clear standards helps increase the accessibility of the language. Also,
  library support from the community. In Go, the libraries for searching and cloning
  repositories from GitHub were immediately clear from a simple Google search, unlike
  for Python. I am a great fit for this because I am an engineer with less than 2-years
  of professional experience. Therefore, having clear standards that are well-documented
  is important for attracting other developers with a similar amount of experience
  to Go. This lack of experience helps remind those with more experience of the
  struggles of a beginner.

  At the end of the talk, I will introduce my tool, namely neighbor
  and quickly demonstrate the problems that it aims to solve (i.e., students in
  academia cloning projects for research (coverage analysis), organizations
  on-boarding new employees, etc.). I am a good fit for this part of the talk because
  at StockX, an immature startup, working on establishing processes still lacks
  a good on-boarding process and tools such as neighbor could help with this. Also,
  my undergraduate research experience helped identify the need for a tool that
  does the "busywork" for an experiment.

6. Tags

  golang, concurrency, github, git, community, standards

---

Personal Details 

## Colton
Name: Colton J. McCurdy
Twitter Handle: @McCurdyColton
Organization/Affiliation: StockX, LLC
Shirt Size: M
Bio: Colton McCurdy is a backend engineer at StockX who has designed, implemented
and maintained many of the company's microservices written in Go. Prior to joining
StockX in 2017, Colton completed his B.S in Computer Science at Allegheny College, where
his research focus was in Mutation Testing which has lead to his newfound interest
in Resiliency (chaos) Engineering. The premise of both Mutation Testing and Chaos
Engineering is to design an experiment --- think of mutated versions of the code
or infrastructure --- that will lead to the propagation of errors.

## Notes
+ three authors, but one presenter
+ the third author is a student
+ also explain that i am the lead author and presenter
+ include all of our names as authors for external visibility (for the college)
+ also make it clear that we dont expect funding for all authors, but additional funding would be helpful
