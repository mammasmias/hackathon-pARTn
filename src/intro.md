# Introduction


Welcome to the pARTn Hackathon!

The hackathon will be held April 1st -- 3rd 2026, at [IRB](./location.md).

Register [here](./registration.md).

## What is this?

### ARTn algorithm

The Activation-Relaxation Technique nouveau (ARTn) is an algorithm for open-ended search of saddle points of a Potential Energy Surface (PES).

ARTn uses the information on local curvature of the PES, to determine a direction of lowest negative curvature.
The atomic system is pushed uphill along that direction, while minimized in all other directions.
After a number of such steps, the system converges to a saddle point of the PES.

### Plugin-ARTn implementation

The plugin-ARTn (pARTn) is an implementation of ARTn as a plugin, i.e. an explicitly external routine to be used by an Energy/Force engine.

Git [repository](https://gitlab.com/mammasmias/artn-plugin), and online [documentation](https://mammasmias.gitlab.io/artn-plugin/) are available.

pARTn is written in modern Fortran, and is interoperable with C through the ``iso_c_binding`` module, and ``bind(C)`` directives.
The interoperability with C is also used to define a python interface ``pypARTn``, and can be used to call pARTn from other languages, i.e. lua.

### Hackathon!

The idea of this hackathon is to go into the very details of pARTn, and attempt to address some issues, or improve on some specifics, or even just apply the code to a particular set of problems.

The first day there will be some talks, going from fairly broad introductory, to narrowing down to the details of pARTn algorithm, and code.
Then, some potential project topics would be presented, which could be picked up by any working group, or just serve as foundation ideas for other ideas.

On the second and third day, the participants wll split into voluntary working groups, each addressing their own chosen problem/project, or any other problem/project they could come up with.

Any potentially interesting work can continue developing after the event, possibly turning into a joint publication.

### Project ideas

Currently some ideas for problems/projects to address are:

- defining benchmarks (i.e. [OptBench](https://optbench.org/) integration, expansion of systems, etc.);
- addressing the soft modes appearing from Lanczos diagonalization: detection, and removal. Possible algorithm branching;
- general way to add custom "modifiers": such as freezing atoms only during particular block of ARTn, etc.
- interfacing into [eOn](https://eondocs.org/);
- can the code execute when on GPU? and/or how to make that possible?
- application to any system a participant might bring up;
- ...

Any other project ideas are welcome!
