# Introduction

## ARTn algorithm

The Activation-Relaxation Technique nouveau (ARTn) is an algorithm for open-ended search of saddle points of a Potential Energy Surface (PES). 

ARTn uses the information on local curvature of the PES, to determine a direction of lowest negative curvature.
The atomic system is pushed uphill along that direction, while minimized in all other directions.
After a number of such steps, the system converges to a saddle point of the PES.

## plugin-ARTn implementation

The plugin-ARTn (pARTn) is an implementation of ARTn as a plugin, i.e. an explicitly external routine to an Energy/Force engine.

Git [repository](https://gitlab.com/mammasmias/artn-plugin), and online [documentation](https://mammasmias.gitlab.io/artn-plugin/) are available.

pARTn is written in modern Fortran, and is interoperable with C through the ``iso_c_binding`` module, and ``bind(C)`` directives. 
The interoperability with C is also used to define a python interface ``pypARTn``, and can also be used to call pARTn with lua.
