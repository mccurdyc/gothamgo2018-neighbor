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

  According to the 2017 StackOverflow survey, approximately 57% of professional
  developers have 5 or less years of experience (https://insights.stackoverflow.com/survey/2017#experience),
  myself included with less than 2 years. It was projected by the Bureau
  of Labor Statistics that by 2020, there would be 400,000 Computer Science
  graduates and 1.4 million professional software engineering jobs (https://obamawhitehouse.archives.gov/blog/2013/12/11/computer-science-everyone).

  To continue the rate of adoption of Go, specifically by the large number of
  developers with less than six years of experience or those not yet programming,
  we as the community, need to continue enforcing and encouraging the many clear
  standards of Go that help make Go more accessible. These well-defined standards
  and the strong and vibrant community are why many of us chose Go as the primary
  language for more than 170,000 projects on GitHub (https://github.com/search?q=language%3Ago).

  In 2018, there were 1.5 times as many projects added to GitHub written in Go
  than in 2017 (https://blog.github.com/2018-11-15-state-of-the-octoverse-top-programming-languages/),
  one of these being our project. A large number of the community members that
  we often see speak can no longer say that their recent project was their first
  open-source project, let alone having been written in Go.

  As a team most of our experience is in languages such as C, Java and Python.
  However, C and Java both lack full-featured libraries for GitHub search and
  cloning and would require more work to wrap those APIs. While Python has library
  support for GitHub interaction, we didn't choose Python due to the lack of clear
  standards around dependency management, packaging, documentation and testing.
  Colton, having recently started at StockX where one of the backend languages of
  choice is Go, became familiar with the language and proposed it for this project.
  While struggling with dependency management, project structure and soon to
  encounter the challenge of supporting concurrency writing the tool in Python,
  we decided to move the project to Go.

  At the end of the talk, Colton will introduce our tool and quickly demonstrate
  the problems that it aims to solve (i.e., students in academia cloning projects
  for research (coverage analysis), organizations on-boarding new employees, etc.).
  The team consists of an Associate Professor who has given over X and Y talks at
  academic and industry conferences, respectively, a software engineer in industry
  at an emerging startup and a student conducting an experiment for his senior thesis.

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
