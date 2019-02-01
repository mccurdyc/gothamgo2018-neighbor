1. Title

  Welcome to the neighborhood: A Tool that Facilitates Concurrent Contributions to GitHub Repositories

2. Elevator Pitch (300 characters)

  When creating neighbor, an extensible tool for analyzing and contributing to GitHub
  repositories, we encountered challenges with package discovery, dependency management
  and concurrency. Go and the community offered solutions for each. This talk also
  explains design decisions of neighbor.

3. Audience Level (Beginner? Intermediate?)

  Beginner

4. Description (seen by attendees)

  When creating neighbor, an extensible tool that leverages advanced GitHub search
  for analyzing and contributing to repositories, we encountered challenges with
  language choice, package discovery, dependency management and concurrent design.
  The lack of a standard for dependency management and poor support for concurrency
  lead us to port the project from Python to Go. With GoDoc and modules, the Go
  community respectively gives a standard for dependency management and a centralized
  resource for package discovery and documentation. In addition to the aforementioned
  offerings, the Go community has well-defined patterns for concurrency. Along
  with introducing the challenges and highlighting the reasons for choosing to
  write neighbor in Go, this talk provides justification for supporting concurrency
  using the fan-out design pattern, explains the steps for identifying and fixing
  race conditions, and highlights the trade-offs between unbuffered and buffered
  channels.

5. Notes (only be seen by reviewers during the CFP process. This is where you
   should explain things such as technical requirements, why you're the best
   person to speak on this subject, etc.)

  According to the 2017 StackOverflow survey, approximately 57% of professional
  developers have five or less years of experience (https://insights.stackoverflow.com/survey/2017#experience).
  To accelerate the rate of Go’s adoption, the community needs to reach this
  demographic of developers by empowering these individual through clear and
  effective standards for package discovery, documentation, dependency management,
  design patterns and one generally accepted way of building systems in Go.
  Colton is one of these professional developers with less than six years of
  experience, who felt productive in Go from day one through the use of GoDoc for
  package discovery and documentation, GOPATH and now modules for managing dependencies
  and following the lead of the community for design patterns for package
  structure and concurrency.

  We wanted to build a tool, named neighbor, that would support advanced GitHub
  search and concurrent analyzation of and contribution to repositories. As a team,
  most of our experience is with programming languages such as C, Java, and Python.
  Since, to our knowledge, both C and Java lack full-featured libraries for GitHub
  search and cloning, we decided not to choose either of these languages. Since
  Python has library support for GitHub interaction, we initially picked it as the
  implementation language for neighbor. However, since we struggled with dependency
  management, project structure, and concurrency issues in Python, we decided to
  port neighbor to Go. Leveraging his experience at StockX, Colton will explain
  the challenges that we faced and the solutions that we implemented in Go.

  We think that developers in both academia and industry will want to use our
  tool to search for, explore, and contribute to GitHub repositories. For example,
  a researcher might want to measure the code coverage of the test suites for the
  thousands Python programs and packages available on GitHub or add or update a
  LICENSE file to all projects under a particular organization. Our tool makes it
  easy for developers to find and clone these repositories and then perform an
  arbitrary command on the source code.

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
StockX in 2017, Colton completed his B.S. in Computer Science at Allegheny College,
where his research focus was in software testing, specifically analyzing a technique
known as mutation testing for evaluating test suite adequacy. Since joining StockX,
Colton has implemented and encouraged others to follow processes for designing,
documenting, reviewing and refactoring software systems.

## Notes
+ three authors, but one presenter
+ the third author is a student
+ also explain that i am the lead author and presenter
+ include all of our names as authors for external visibility (for the college)
+ also make it clear that we dont expect funding for all authors, but additional funding would be helpful

## Greg
Name: Gregory M. Kapfhammer
Twitter Handle: @GregKapfhammer
GitHub: https://github.com/gkapfham
Web: https://www.gregorykapfhammer.com/
Organization/Affiliation: Allegheny College
Shirt Size: L
Bio: Gregory M. Kapfhammer is an Associate Professor in and Chair of the Department of Computer Science at Allegheny College. He is an award-winning educator with twenty years of experience in teaching software engineering and software testing to graduate, undergraduate, and high school students. Collaborating with a diverse and highly skilled group of researchers and engineers, Gregory has given presentations at a wide variety of conferences, including the International Conference on Software Testing, the International Conference on Automated Software Engineering, PyOhio, PyGotham, and the PyCon Education Summit. Along with teaching courses and conducting research, Gregory implements, tests, documents, and debugs open-source software available on GitHub.

## Saejin
Name: Saejin A. Mahlau-Heinert
Github: https://github.com/michionlion
Web: https://saejinmh.com
Shirt Size: L
Bio: Saejin Mahlau-Heinert is a Computer Science major at Allegheny College. He is a teaching assistant for many upper-level courses, as well as a collaborator or lead on numerous departmental software development efforts. Saejin has done work in many different areas, including esoteric programming languages, standards-based grading, game design, virtual reality, and ray-tracing. His variety of interests led to an appreciation for good development and research tools such as neighbor. Besides thesis and teaching work, Saejin enjoys integrating technology and art, exhibiting related works at Allegheny’s art gallery.
