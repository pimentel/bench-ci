# bench-ci

A continuous integration tool focused around benchmarks where the best you can do is give an estimate rather than exactly the "correct answer."
The main focus is around ensuring that performance of a tool (in terms of "error") does not degrade overtime.
While standard continuous integration tools allow for integration of testing frameworks, there does not appear to be a good tool for keeping track of metrics that are inherently fuzzy.
The use cases that I have in mind are:

- estimation of parameters (in a statistical sense)
- prediction error (in a machine learning context)
- estimation of false discoveries as well as power (in a statistical sense)

## current status

Currently this is only a rough idea and there is no implementation.
This project grew out of my need for continuously benchmarking tools such as
[kallisto](https://github.com/pachterlab/kallisto) and [sleuth](https://github.com/pachterlab/sleuth)
where tests only guarantee "correctness" of the code, not necessarily of the algorithm.

I am currently looking for people who are interested in developing this with me, as well as people who have opinions on the types of things that should be incorporated in the first prototype.
I plan to have a prototype by the end of the year, but we will see how that works out. : -)

Please make any comments/suggestions for features under the [github issues tab](https://github.com/pimentel/bench-ci/issues)

# requirements

## setup

Setup should include an array of benchmarks.
`bench-ci` should not be involved in actually making the benchmarks.
Instead, benchmarks should be an external command.
Configuration should also be available via a online interface.
`bench-ci` should be configured on a project by project basis, much like travis-ci.

## execution

- should be able to be called remotely potentially from some trigger (github?)
- should be able to be manually called locally (command line)

## git integration

- should be able to keep track of different versions according to SHA1 hash or tag
- should be able to keep track of different branches
- should be able to deal with private repositories (API tokens and keys)

## modeling

- should be able to keep track of several different errors and statistics per benchmark
  - especially important to keep track of training, validation, and test datasets
  - several different versions of error

## interface

- there should be a web application that reads data that is stored (technically anywhere) and can make summary reports
- there should be plotting functionality in order to visualize the performance over time of different metrics

## implementation

- I am currently thinking of doing this as a node package

### useful libraries

- [NodeGit](http://www.nodegit.org/guides/)
