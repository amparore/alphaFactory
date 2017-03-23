
HOW TO COMPILE:

alphaFactory requires Boost-C++ (version 1.60 or greater), and optionally gmp.
It also requires a C++11 or better compiler.

alphaFactory is known to compile on MacOSX and Linux with this command:

 * Boost version:
   g++ -I/usr/local/include -L/usr/local/lib alphafactory.cpp  -std=c++11 -O2 -o alphafactory

 * GMP version:
   g++ -I/usr/local/include -L/usr/local/lib -DUSE_GMP=1 alphafactory.cpp  -std=c++11 -O2 -lgmp -o alphafactory



//=============================================================================

HOW TO RUN:

The command has this form:

./alphaFactory  "function"  <CTMC rate>  <accuracy>

The description of the function grammar is found in alphaFactory.h

These examples show how to run the tool:

./alphafactory '0.3*I(5) + 0.5*I(10)' 3.0 0.0000001
./alphafactory 'Erlang(0.75,4)' 1.25 0.0000001
./alphafactory "Triangular(2,6)" 0.85  0.0000001
./alphafactory "27/10 * Exp(-3 * x) * x + 2/5 * Exp(-2 * x) * Pow(x,2) + 1/10 * Exp(-1 * x) * Pow(x, 3)" 1.5 0.0000001

A unit test can be run using:

./alphaFactory test



//=============================================================================

HOW TO USE THE API:

Read alphaFactory.h for the description of the exported C++ API functions.
