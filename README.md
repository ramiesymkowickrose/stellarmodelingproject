# stellarmodelingproject
UC Berkeley Physics 77 final project seeking to produce a light-weight model for the stellar evolution of mainphase stars, based on the 1D Modeling Methods used by conventional modeling programs like MESA. 
In order to rapidly acheive approximations on lower-end hardware, this program neglects:
* Convection
* Chemical transportation
* Chemical Composition asside from percentage hydrogen available
* Spin
## Dependencies
This program is dependant on numpy, pyplot, scipy, and pynucastro. It uses rates from the JINA Reactlib Database included in pynucastro for the purpose.

## Usage instructions
The model uses a class based structure, initializing an object called MainphaseStar with a series of  arrays containing temperature by radius (in K), density by radius (g.m^-3), pressure by radius (N.m^-2), luminosity by radius (MeV), and percent hydrogen by radius, as well as an integer containing the total radius (m) Initial radial cells are assumed to be of uniform radial increments. The primary method for performing stellar evolution computations in the class is masssolve, which takes an input array of masses for which the system will be solved on. This will return a series of arrays that describe the structure of the star.

