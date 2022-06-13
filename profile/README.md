# Organization stuff

Below are the standards that the team is aspiring to maintain. The principle underlying all of it is: ease. We want to maximize ease of reading the code, contributing to it, and understanding/accessing the data products. 

1. Written in python 3, following PEP8
2. Missing/bad data flag is NaN. Not 0. Not -1. Certainly not a combination of different things. Consistent across all data levels. 
3. Clean Code practices will be followed as much as possible. 
   * Variable names are verbose but concise to their scope
   * Functions should only be a few lines long each (e.g., roughly < 10)
   * The level of abstraction of every line of code should correspond to its neighboring lines of code
   * When there’s no better way to do something so you have to loop -- make the loop as few lines as possible so it’s easy to follow (use the related-level-of-abstraction concept from functions above)
   * Code should be written to work, then refactored for clarity, to reduce duplication (abstract that stuff away to a function callable from anywhere in the class, or step up to a higher class if it’s reusable beyond just this class)
   * Functions should have very few inputs and only one output -- exceptions allowed but both should be minimized. A function does _one_ thing
4. Tests should be implemented and include a codecov metric
5. We’ll implement continuous integration on GitHub -- probably via TravisCI
6. If packages already exist to do a thing well, use them (e.g., sunpy, astropy, numpy, pandas, etc)
    * We will build with sunpy integration, in particular, in mind from the start. 
    * astropy units will be used everywhere it adds value. 
8. Create yaml environment files that include versions on all of the dependencies
9. Particular effort should be made for documentation of tools likely to be used by the community (e.g., level 1 to 2 processing for turning images into CME kinematic profiles)
10. Always keep in mind that this mission is a useful part of the HSO, so all of our products, code, coordinate systems, documentation, etc should make it highly compatible with other datasets 
11. Data products will be versioned to correspond to the code found in the repositories herein
