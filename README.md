# Recombination Simulations
set of scripts to process simulations to be used for assessing whether LDhelmet will accurately infer recombination rates from our population samples

### Justification

Recombination maps can be inferred using haplotypes sampled from natural populations. Prorams like LDhat and LDhelmet estimate the rates. LDhelmet has been shown to provide higher accuracy maps for species with higher mutation rates (i.e. mice versus humans).

1. Given that we have only a sample of 10 diploid individuals (i.e. 20 alleles) the first step is to test whether we can accurately estimate rho (4Ner) from our sample
2. The key parameter in LDhelmet is the block penalty. Using simulated data, with arbitrary maps, we can look at what block penalties will work best for our particular data
3. To infer haplotypes from our genome sequencing data: We will use ShapeIt2 which uses both LD in a sample as well as phase-informative reads to estimate haplotypes. However, we need to get an estimate of the error in this approach to see whether it will severely bias our recombination maps. With a given switch error rate we can incorporate that into simulations and then run LDhelmet.

The scripts in this repo allow you to get fasta sequence from SLiM output by giving the simulated chromosome a similar base composition to mice (in our case).
