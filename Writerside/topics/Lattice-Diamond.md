# Lattice Diamond

A short, dumb guide to using Lattice Diamond for programming ECP5 series FPGAs.

This is largely a text version of [this wonderful video](https://www.youtube.com/watch?v=SmdEP_ZsBgM), as well as
notes of what I have found as useful info. Farrell, if you're out there, my sincere thanks, documentation is crazy
hard to find, your vid was amazing!

With that out of the way, this guide aims to cover the following:
1. Project creation
2. Pin configuration
3. Using pre-configured blocks
4. Simulating code
5. Creating a simple 4 by 4 bit adder circuit

This will *not* be covering:
1. Installation of Diamond
2. Licensing of the software (the free license will be utilized)

This guide will use, as a reference, the [ULX3S](https://ulx3s.github.io/) by [Radiona](https://radiona.org/), an
open-source FPGA solution which I absolutely fell in love with.

![ULX.jpg](ulx3s.jpg)
Fig.1.: Radiona ULX3S board