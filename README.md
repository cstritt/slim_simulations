# Slim Simulations

This folder contains the code to simulate a bacterial within-host metapopulation using SLiM (https://messerlab.org/slim/), as described in Stritt & Gagneux 2022 (https://doi.org/10.32942/X2GW2P):

"Infection begins with a single bacterium giving rise to an exponentially growing population through clonal reproduction and 19 "empty" populations. Once this pop
ulation reaches carrying capacity K = 20, 000, it can seed new populations (Figure B1a), which again grow and can seed new populations when K is reached. More specifically, each generation a number of n migrants is drawn from a Poisson distribution with mean 1; n individuals are then drawn from a random population that has reached K and migrated to a random empty population until all populations are occupied. Exemplary growth dynamics of the simulation are depicted
in Figure B1b. Mutations are simulated at a rate µ = 5 × 10−10 /bp/gen in a genome of 4 Mb. Selection is either assumed to be absent (s = 0) or purifying (s = −9.5e − 4), as proposed by Pepperell et al., 2013. The simulation ends after 70 generations, which with a generation time of 24 h corresponds to a 10 week infection."

The script can be run from the SLiM GUI or from the command line, like this:

```console

    slim \
      -d "outAll='outputAll.s_${s}.m_${m}.tsv'" \
      -d N=20 -d K=5e4 -d gs=4e6 -d Mu=${m} -d s=${s} \
      granuloma_metapopulation.slim

```

The -d parameter allows to define different parameters: 

    N: number of subpopulations
    K: carrying capacity
    gs: genome size
    Mu: mutation rate
    s: selection coefficient
    outAll: output file containing information on all mutations in the last generation
    outInd: output file containing the number of mutations of all strains in the last generation
