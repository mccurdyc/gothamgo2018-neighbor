Use this for brainstorming about the proposal

### Resources
+ https://www.oreilly.com/conferences/sample_proposals.html#tech
+ https://bridgetkromhout.com/blog/give-actionable-takeaways/

## Talk Outline

+ community
+ library support
+ concurrency
  + pipelines; namely fanout
  + channels; guaranteed delivery
  + race conditions (and detection)
+ originally started in Python
  + spent a lot of time figuring out how to manage dependencies
    + at a high-level there is no community standard
    + `requirements.txt`
    + pipenv
    + virtualenvs
    + there is a 2-hour, \$50 course for managing dependencies! (https://training.talkpython.fm/courses/explore_python_dependencies_course/managing-python-dependencies-with-pip-and-virtual-environments)
  + inaccessibility of concurrency
      + show an example (ask Dr. Kapfhammer for help)
  + Google search: "python search repo github" versus "golang search repo github"
    + i.e., the answer was not clear with the python search
+ what problem neighbor aims to solve (story)
  + examples
    + `go cover`
    + getting a new developer started at your company

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

---

Bridget's Thoughts

Title

- In a single-track event, an attention-grabbing title isn't as essential.
  However, when I looked at your list of titles, I immediately thought "Won't
  You Be My Neighbor? A Tool for Multi-Project GitHub Search" would be a fun title.

- Capitalize the word after the hyphen if it would be capitalized on its own.

- The others are okay, though avoid "handyman" because it's gendered. (I would
  downvote a talk that made me think "annoying tech bro who doesn't consider how
  women/enby techies will feel upon reading the title".)

- Complex phrases like "multi-project GitHub search and arbitrary concurrent
  exploration" don't belong in industry conference talk titles (even though yes,
  I know academia uses titles like this). They can go in the short or long
  description. When I look at "Multi-project GitHub Search and Advanced Concurrent
  Repository Exploration in Go" It's entirely too much to digest, mentally.
  **All that extra detail gets lost in the title, and would be better in the description.**

Elevator Pitch (Or, short description)
- You say "we" and explain it in the notes to the committee, but your collaborators
  don't make much of an appearance on GitHub. That's confusing (though it does
  appear that active development might be happening elsewhere)?

Talk Outline
- There are two sections entitled this, in https://github.com/mccurdyc/gothamgo2018-neighbor/blob/mccurdyc/rough-draft/proposal/NOTES.md.
  The first one spends way too much time establishing the scene. The second one is
  better, but while you want the takeaways, it might be awkward to lead with them.
  Start with the pain point. You can backtrack to technical detail, but you
  only get one chance to capture people's imaginations. Get to the "Why" as soon as you can.

Other thoughts: "The Go community offers a clear standard going for dependency management"
Granted I'm not really in the Go community, but I read that and first I'm like
"is there a new standard called "going"? and also I'm skeptical because I see the drama around dep.

In the future work section, are those 5-8 case studies in progress? Or are you
saying you would want there to be some case studies?

Bio: Consider using the Oxford comma, and your use of "has lead" should be "has led".
(The latter is a highly common error.)

In general: I chatted with one of the organizers because I wanted to make sure
that they didn't require large-scale production use cases. They don't care about
that, which is great (whereas most confs I'm involved with want to know how things
scale). **They care about variety and innovative ideas, so you probably want to make
sure you're highlighting how this is different from other tools and why you wrote
this instead of adapting/repurposing something out there.**

Your language is a bit formal/academic. It's possible you plan on also submitting
this to academic conferences. **If you don't, then it's okay to make it a bit more
storytelling-ish.** "When we tried to foo and bar, we ran up against a brick wall
of baz." "Solving our foobar problems gave us X and Y, which we expected, but
Z was an unanticipated bonus!" A bit more conversational, basically.

Overall, this is good stuff. They care that something seems well thought out, which yours is

I'd be happy to look again in the next couple days if you want!
