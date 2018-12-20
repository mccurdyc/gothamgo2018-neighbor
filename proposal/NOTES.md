Use this for brainstorming about the proposal

## General Thoughts

+ neighbor is an enabler
+ neighbor takes the busy work out of cloning multiple projects, focus on what you need
+ you don't need to learn the GitHub API
+ saves X developer hours by not requiring to learn the API, implement in their language of choice
+ also, on top of saving developer hours to learn how to interact with GitHub, concurrency is another problem
+ GJ Hellfont
  + "trivial" contribution
+ becomes the standard way of obtaining sample projects from GitHub for research
  + helps threats to validity
  + research groups "hand-picking projects"
  + research groups currently hire RAs to obtain projects
    + not a great use of a RA's time
+ less of a tool pitch and more of a "lessons learned" talk

### Potential Use Cases of neighbor
+ at a start-up where you typically "buy" over build
  + switching CI tools on all of our projects (tedious, repetitive process)
+ new employee on-boarding
  + clone these projects (specified by a GitHub query)
  + could also have a "plugin" for doing certain things in those projects (pulling in dependencies, etc.)
+ solves "Just hire graduate students to do it"

## Brainstorming Titles
+ The Neighborhood Handyman: something more technical as the subtitle
+ The Friendly Neighbor: a standardized and efficient enabler for multi-project
  GitHub tasks
+ neighbor: a tool for multi-project GitHub search and arbitrary concurrent exploration
+ **neighbor: a tool written in Go for multi-project GitHub search and arbitrary concurrent exploration**
+ The lessons learned from writing a tool in Go for multi-project GitHub search and arbitrary concurrent exploration

## Talk Outline
Lessons will include:
+ language choice
  + first, used Python (library support for interacting with GitHub was not great)
    + what was lacking in library support in Python (this is a question I get a lot when pitching the idea)
  + Go has `google/go-github` and `src-d/go-git`)
  + Go's support and accessibility for concurrency
    + maybe include a snippet of concurrent code in Python?
+ concurrency pipelines
  + fanout
  + point audience to good references for pipelines since it is out of the scope of this talk
+ race condition (and detection)
  + quickly, what is a race condition
  + **what was the specific race condition in our code**
    _I need to revisit this (there should be the old PR)_
  + mention the `-race` flag
      + why does `go build -race ...` not show me my race conditions!?
        + build-time race conditions
      + run-time race detection `go run -race ...`
+ channels (buffered v. unbuffered)
  + why we chose to use unbuffered channels
    + mainly guarantees (in an academic context, for research, this is important)

[Problem]
1. tell a story with a pain-point
  + there was a student earlier this year working on their capstone project
    + TODO: major points in the story

[Solution]
2. what is neighbor
  + catchy phrase, "the helpful neighbor"
  [Problem]
  + what problems does neighbor solve

[Solution]
3. why use neighbor over doing writing the code to clone, etc. yourself?
  + concurrency
    + efficient
    + thread-safe
  + thoroughly-tested
  + saves time
    + developers don't have learn the intricacies of the GitHub API
    + developers don't have to write the concurrent code
      + writing concurrent code is difficult [TODO cite Herb Sutter (http://www.gotw.ca/publications/concurrency-ddj.htm)]
4. implementation details
  + _gothamgo talks seem to really focus on why Golang_
    + originally started with Python
      [Problem]
      + lacking a good GitHub library
      + would have to write the wrapper for the API
      [Solution]
    + Go had great libraries in `google/go-github` (for searching), `src-d/go-git` for cloning (doing `git` things)
      [Solution]
    + great concurrency support built into the language
    + concurrency pipelines
5. future work/goals/bigger picture ideas
  + 5-8 case studies
    + concurrency v. sequential
    + industry use
    + academic use (Dr. Kapfhammer mentioned over the summer)
  + GitHub hard API limits of 1000 projects at a time
    + to get around this, we could hit the API multiple times with a moving-window approach
  + consider disk space
    + potentially add pagination based on disk space
    + remove/compress (maybe having the analyzed source code is important) a project's source after exploration
6. invitation to start using the tool
