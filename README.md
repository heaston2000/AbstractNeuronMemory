# Pattern Recognition and Recollection in an Abstract Neuron

This repository contains simulations written in MATLAB Live Scripts for my 2023 thesis for the mathematics major at Middlebury College.

Memory recollection and the ability to reconstruct signals from partial input is one of the most important capabilities and deepest mysteries of the biological neuron. A suite of models have been designed to understand and imitate this power of the brain, based on the hypothesis that learning occurs through the changing of synaptic connections in the neuron. Here, we pursue the analysis of Hebbian-based models (the Simple Hebbian Model, Oja's Rule, and the BCM Model), all based on the notion that if a neuron persistently takes part in the firing of another neuron, their connection will become stronger. We analyze the utility of each of these rules in both a biological and computational context. Through stability analysis and simulation, we show the instability and shortcomings of the Hebbian Rule, the stability and ability to recognize patterns of Oja's Rule, and the BCM Model's unique ability to reconstruct and recollect patterns.

## Two documents are present:
- *HebbianOjaSimulations.mlx* - Simulations run on abstract neurons trained with both the simple Hebbian Rule and Oja's Rule.
- *BCMSimulations.mlx* - Simulations run on abstract neurons trained with the BCM Rule.

Further details are available in each of the live scripts. The simulations performed for the Simple Hebbian and Oja Rules follow the input schemes:
1. Just noise as input. Each input dimension is sampled uniformly from 0 to 1.
2. Just patterned input, each input is 0.1, except for that in dimension 1 which is equal to 5.
3. 95% noise and 5% patterned input. Inputs are described above but each is randomly sampled, with noise being sampled with probability 0.95.
4. The last simulation stimulates the neuron with solely patterned input then noise for the remainder,  after enough time, the neurons are occasionally triggered by the pattern again to test their abilities to recall it.

The simulations performed for the BCM Rules follow the input schemes:
1. The test done in Udeigwe et al. using contrived outputs that conform to our stability requirements. This test demonstrates the selectivity this training rule demonstrates between outputs.
2. A test similar to the one done for the Simple Hebbian and Oja Rules for differentiation between patterned and random inputs. (95% random and 5% patterned input with identical magnitudes).
3. A test done for "recollection" with the inputs devised by Udeigwe et al. (This simulation is not used in the thesis). The neuron is exposed to a pattern for a certain amount of iterations then solely exposed to another one before being re-triggered with the first to test its recall ability.
4. The same test done for recall ability that is performed for Oja's Rule. This time the neuron is exposed to a pattern for an initial period, then exposed to only random noise for the rest of the duration. Outputs to both the noise and the pattern are monitored even when the neuron is not receiving the patterned input. 
