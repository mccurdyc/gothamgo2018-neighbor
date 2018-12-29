# Multi-project GitHub search and arbitrary concurrent exploration in Go

## Description

Go has excellent library support for interacting with projects on GitHub and
writing concurrent applications is more accessible than in languages, such as Python.
While creating neighbor, a tool for dynamic GitHub repository searches and arbitrary
concurrent exploration in Go, I encountered common obstacles such as designing
a pipeline for processing results, race conditions, trade-offs between unbuffered and buffered
channels and more.

## Abstract

In this talk I will discuss the challenges faced and lessons learned while creating
my first personal open source tool in Go. This project helped identify the importance of
community and clearly-defined standards. From both a negative and positive perspective
with the numerous competing standards for dependency management with no clear
"leader" in Python and the clearly-defined pipeline techniques in Go, respectively.
Having clear standards helps increase the accessibility of the language. Also,
library support from the community. In Go, the libraries for searching and cloning
repositories from GitHub were immediately clear from a simple Google search, unlike
for Python. At the end of the talk, I will introduce my tool, namely neighbor
and quickly demonstrate the problems that it aims to solve (i.e., students in
academia cloning projects for research (coverage analysis), organizations
on-boarding new employees, etc.).
