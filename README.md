# Slim Simulations

This folder contains the code to simulate a bacterial within-host metapopulation using SLiM (https://messerlab.org/slim/), as described in Stritt & Gagneux 2022:

"Infection begins with a single bacterium giving rise to an exponentially growing population through clonal reproduction and 19 "empty" populations. Once this pop
ulation reaches carrying capacity K = 20, 000, it can seed new populations (Figure B1a), which again grow and can seed new populations when K is reached. More specifically, each generation a number of n migrants is drawn from a Poisson distribution with mean 1; n individuals are then drawn from a random population that has reached K and migrated to a random empty population until all populations are occupied. Exemplary growth dynamics of the simulation are depicted
in Figure B1b. Mutations are simulated at a rate µ = 5 × 10−10 /bp/gen in a genome of 4 Mb. Selection is either assumed to be absent (s = 0) or purifying (s = −9.5e − 4), as proposed by Pepperell et al., 2013. The simulation ends after 70 generations, which with a generation time of 24 h corresponds to a 10 week infection."