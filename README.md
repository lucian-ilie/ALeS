# ALeS: Adaptive-length spaced-seed design

**Author:**

Arnab Mallik, Lucian Ilie
Yiwei Li (amallik3@uwo.ca), Lucian Ilie (ilie@uwo.ca)
Department of Computer Science
The University of Western Ontario, London, Ontario, Canada

**Description:**

Similarity search is one of the most critical challenges in bioinformatics. It is time and memory intensive, hence heuristic methods using multiple spaced seeds are commonly employed. A spaced seed is a string of matches interspersed with don’t care positions. Sensitivity, the probability of hitting a similarity region, is used to evaluate their quality. High sensitivity increases the probability of detecting more remote homologs.

We present ALeS: Adaptive-length spaced-seed design, a software program to generate highly sensitivity seeds. It uses two novel optimization techniques: indel optimization and adaptive length. In indel optimization, a random don’t care position is either inserted or deleted, following the hill-climbing approach with sensitivity as cost-function. In the adaptive length algorithm, the seed lengths are modified using previously found good seeds. It consistently outperforms all leading programs used for designing multiple spaced seeds like Rasbhari, AcoSeeD, SpEED, and Iedera.

ALeS will benefit numerous software programs in a variety of areas, including traditional ones, such as PatternHunter for similarity search, SHRiMP and BFAST for read mapping, bestPrimer for designing primers, as well as emerging topics, including alignment-free comparisons and evolutionary distance programs, such as protSpaM, MultiSpaM for phylogeny reconstruction.

**Installation:**

g++ compiler is required to run ALeS.
Download all files from the repository, navigate to ALeS directory and compile ALeS.cpp using the **make** command.

**How to run ALeS:**

Use the command format as shown:

```
./ALeS <weight_of_seed> <number_of_seeds> <similarity> <region_length>
```
For example,
```
./ALeS 10 4 .75 50
```
This will generate 4 spaced seeds, each of weight 10 having similarity level of 0.75 for region length 50.



