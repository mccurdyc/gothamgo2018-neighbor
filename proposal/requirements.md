1. Title

  Multi-project GitHub search and arbitrary concurrent exploration in Go

2. Elevator Pitch (300 characters)

  Go has excellent lib support for interacting with GitHub and writing concurrent
  code. While creating a tool for dynamic repository search and arbitrary concurrent
  exploration, I encountered common obstacles such as concurrent design, un- v. buffered
  chans and the importance of community standards.

3. Audience Level (Beginner? Intermediate?)

  Beginner

4. Description (seen by attendees)

  Go has excellent library support for interacting with projects on GitHub and
  writing concurrent applications is more accessible than in languages, such as Python.
  While creating neighbor, a tool for dynamic GitHub repository searches and arbitrary
  concurrent exploration in Go, I encountered common obstacles such as designing
  a pipeline for processing results, race conditions, trade-offs between unbuffered and buffered
  channels and the importance of community standards.

5. Notes (only be seen by reviewers during the CFP process. This is where you should explain things such as technical requirements, why you're the best person to speak on this subject, etc.)

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

  golang, concurrency, github, git

---

Personal Details 

## Colton
Name: Colton J. McCurdy
Twitter Handle: @McCurdyColton
Organization/Affiliation: StockX, LLC
Shirt Size: M
Bio: Colton McCurdy is a backend engineer at StockX who has designed, written
and maintained many of the company's microservices written in Go. Prior to joining
StockX in 2017, Colton completed his undergraduate degree at Allegheny College, where
his research focus was in Mutation Testing which has lead to his newfound interest
in Resiliency (chaos) Engineering. The premise of both Mutation Testing and Chaos
Engineering is to design an experiment --- think of mutated versions of the code
or infrastructure --- that will lead to the propagation of errors.

## Dr. Kapfhammer
Name:
Twitter Handle:
Organization/Affiliation:
Shirt Size:
Bio:

## Saejin
Name:
Twitter Handle:
Organization/Affiliation:
Shirt Size:
Bio:

---

Additional Information:

This is probably where we include the multi-speaker information (I think we should discuss).
Also flight information. Links to prior presentations.

