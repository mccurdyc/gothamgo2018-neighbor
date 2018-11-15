Use this for brainstorming about the proposal

## General Thoughts

+ neighbor is an enabler
+ neighbor takes the busy work out of cloning multiple projects, focus on what you need
+ you don't need to learn the GitHub API
+ saves X developer hours by not requiring to learn the API, implement in their language of choice
+ GJ Hellfont
  + "trivial" contribution
+ becomes the standard way of obtaining sample projects from GitHub for research
  + helps threats to validity
  + research groups "hand-picking projects"

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

## Talk Outline
1. what is neighbor
  + catchy phrase, "the helpful neighbor"
  + what problems does neighbor solve
2. why use neighbor over doing writing the code to clone, etc. yourself?
  + concurrency
    + efficient
  + thoroughly-tested
  + saves time
    + developers don't have learn the intricacies of the GitHub API
3. future work/goals/bigger picture ideas
4. implementation details
  + _gothamgo talks seem to really focus on why Golang_
    + originally started with Python
      + lacking a good GitHub library
      + would have to write the wrapper for the API
    + Go had great libraries in google/go-github (for searching), src-d/go-git for cloning (doing `git` things)
    + great concurrency support built into the language

## Future Work
+ 5-8 case studies
  + industry use
  + academic use (Dr. Kapfhammer mentioned over the summer)
