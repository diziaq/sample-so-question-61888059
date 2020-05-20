####This project is a demo for a problem.

#####Set up:
Module `sub-donor` is a java module:
- contains ont public class Cowboy
- exports nothing (`module-info.java` has empty body)

Module `sub-recipient` is NOT an exlicit java module(`module-info.java` is absent)

#####Problem
Class `Cowboy` from `sub-donor` is visible for `sub-recipient`,
what causes `Main` class to compile succesfully.
Although it is expected that all classes of `sub-donor` are invisible outside the package.

#####Note
Nevertheless, classes of `sub-donor` are invisible for other modular projects.
It is easy to see: after adding a `module-info.java` into `sub-recipient`
the project ceases to be compiled.
