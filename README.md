# bench-ci

A continuous integration tool focused around benchmarks where there is no "right answer".
The main focus is around ensuring that performance of a tool (in terms of "error") does not degrade overtime.
While standard continuous integration tools allow for integration of testing frameworks, there does not appear to be a good tool for keeping track of metrics that are inherently "fuzzy".
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
