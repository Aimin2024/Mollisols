This numerical simulation is made to estimate the effect of soil mixing on luminescence ages under different scenarios (i.e., steady mixing on stable soil surface versus mixing within an aggrading soil surface) .

Assumptions of the Simulation

The soil space is treated as infinite, with no material loss and a consistent dose rate over time. To investigate the downward mixing of the soil body, we divided the soil matrixprofile into individual layers (0.05m each layer) based onaccording to their depths. Soil disturbance is reflected in the translocationtransport of particles frombetween different layers. The disturbance intensity is indicated by the likelihoodprobability of particles transporting from the i th layer migrating to the j th layer. Hence, the downward overall mixing characteristics of the entire soil profile can be expressed by thea probability matrix of particle migration. Correspondingly, the j th layer has a reception probability for particles from the i th layer. The matrix of reception probabilities (MRP) also reflects the disturbance characteristics of the profile. To facilitate calculation, the numerical simulations are based on the MRP. In this simulation, only downward mixing, with the intensity decreasing with depth, is considered. This allows for the simultaneous check of the proportion of zero-age grains.

The evolution of soil downward mixing over time is examinedassumed atwith a step size of 0.03 ka increments. A total of 1,000 mixingdisturbance cycles, equating tospanning a time duration of 30,000-year30 ka timespan, was simulated. At the very beginning of the simulation, each soil layer has an originalinitial depositionalburial age calculated as the ratio of its depth (m) to the accumulation rate (m/ka). Prior to the onset of a mixing cycle, the luminescenceburial age of particles from all but the uppermost layer, is increased by 0.03ka. The luminescenceburial age of particles from the uppermost layer shall remainis set as 0 ka allthroughout the timeprocess to simulate the “bleaching” of luminescence signals due to light exposure of grains onnear the soil surface. During the period of each mixing cycle, each layer randomly receives particles from one of the otherupper layers with a given probability. At the end of the disturbancea cycle, the age distributions of the whole profileindividual layers are updated.

After 1,000 cycles of mixing, we conduct random sampling for each layer forwith a sample size of 120,000 times to formobtain the age distribution of each layer. Random noise of 10% is subsequentlyis added introduced to these obtained distributionssimulated ages to simulateaccount for uncertainties arising from laboratory measurement. The relative standard deviation (RSD), the proportion of pseudo-zero-age grains that have pseudo-zero ages (i.e., those with an age not exceed 0.2 ka), and the k/pmax for the age distribution of each layer are then calculated. TThe RSD reflects the scatter of the datasetsimulated ages., It roughly corresponds towhich resembles the overdispersion (OD) parameter calculated fromin the central age model that calculates the scatter of distribution in a logarithmic scale. in the text.. The ratio of k to pmax is obtained by unmixing the age distribution into a series of normal distributions. Considering errors, zero-age grains are taken as particles with an age of less than 0.02 ka. The acquisition of the k/pmax is implemented through the attached “unmixNORM” R function.

Scenario with steady surface

In this scenario, the depth of the soil body is set as 2 m and remains unchanged throughout the simulation. The soil body is divided into 40 layers at an interval of 0.05 m. To set the downward mixing intensity decreasing with depth, the MRP mainly considers two aspects: 1)The probability matrix describing the downward mixing of grains between different layers is set such that As depth increases, each(1) the probability of receiving grains from upper layers decreases as the depth of the considered layer increases and (2) the probability of receiving grains from upper layers decreases as the distance between the upper and considered layers increases . These ensure that the degree of downward mixing decreases as the depth of a layer increases. layer increases the likelihood of receiving (or retaining) particles from itself. This means that particles are less likely to migrate to other layers and at the same time, it is less likely to receive grains from other layers. 2) As depth increases, the proportion of particles from the soil surface gradually decreases.

Scenario with accumulation at the surface

In this scenario, the initial depth of the soil body is set to be 0.15 m and contain only 3 layers. The accumulation rate of dust at the surface is assumed to be a constant value of 0.065 m/ka. The setup of the MRPprobability matrix is similar to the scenario with steady surface. The only difference is that the MRP matrix will be updated with the increase of depththe number of layers due to dustsoil accumulation at the surface.
