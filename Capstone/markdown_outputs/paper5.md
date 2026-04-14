<!-- image -->

## Full Length Article

## Critical evaluation of the pulsed selective laser melting process when fabricating Ti64 parts using a range of particle size distributions

Abdullah Yahia Alfaify a , b , ∗ , James Hughes a , Keith Ridgway a

- a The Advanced Manufacturing Research Centre with Boeing, The University of Sheffield, Wallis Way, Rotherham, Sheffield, S60 5TZ, UK
- b Industrial Engineering Department, College of Engineering, King Saud University, P.O. Box 800 Riyadh 11421, Saudi Arabia

## a r t i c l e i n f o

Article history: Received 24 May 2017 Received in revised form 17 October 2017 Accepted 10 December 2017

Available online 16

December 2017

## Keywords:

Pulsed selective laser melting Layer thickness Particle size distribution Process parameters

Ti64

## 1. Introduction

Powder bed metal additive manufacturing (PB-MAM) processes such as selective laser melting (SLM) and selective laser sintering (SLS) are used to fabricate metal parts directly from metal powder by adding layers of powder. There are three main steps in PB-MAM: (1) spreading the powder as a layer, (2) selectively melting the powder according to a CAD file and (3) lowering the platform. These steps are repeated until the part is completely built. A range of systems have been classified under the technologies of energy source, fabrication process, and the form of raw materials as described in the work of Frazier [1], Gu et al. [2] and Herderick [3].

In powder-based metal additive manufacturing systems, powder characteristics are critical because they affect the process efficiency and the quality of built parts, therefore it is essential that process parameters are selected accordingly. The spherical shape of powder particles (powder particle morphology) and proper particle size distribution facilitate good packing density and con-

∗ with

Corresponding author at: The Advanced Manufacturing Research Centre Boeing, The University of Sheffield, Wallis Way, Rotherham, Sheffield, S60 5TZ, UK. E-mail addresses: aalfaify@ksu.edu.sa, aymalfaify1@sheffield.ac.uk (A.Y. Alfaify), j.hughes@sheffield.ac.uk (J. Hughes), k.ridgway@sheffield.ac.uk (K. Ridgway).

## a b s t r a c t

Selective Laser Melting (SLM) is a metal additive manufacturing process where parts are fabricated from metal powder based on CAD data. Selection of the best process parameters for the pulsed SLM processes is a fundamental problem due to the increased number of parameters that have a direct impact on the melt pool compared to the continuous SLM processes. In previous studies, volumetric energy density or scan speed have been used as control variables for applied energy. In this paper, the process parameters (laser power, exposure time, point distance and hatching distance) were considered individually, in addition to particle size distribution and layer thickness. The Taguchi experimental design method was used to determine and optimise the effect of the selected input parameters. The effect of exposure time and its correlation with layer thickness and particle size distribution was then investigated. The results show the best combination of process parameters which can provide fully or near fully dense parts. The results also show the minimum exposure time that can be used with different powder types and layer thicknesses. The paper concludes with a study which shows the part location has a significant impact on sample quality.

© 2017 Elsevier B.V. All rights reserved.

tribute to fabricating parts with good mechanical properties. Large amounts of fine particles will affect the flowability of powder which may lead to an inconsistent powder layer. Insufficient powder can cause voids between powder particles resulting in poor density and uneven surface roughness. The percentage of fine particles to coarser grains should be considered to minimise voids and produce fully or near fully dense parts [4].

A number of previous studies have investigated the influence of the laser power source on part density. Demir et al. [5], when using a pulsed wave SLM system to build 18Ni300 maraging steel, found that with a fixed energy density, exposure time plays a major role in improving part density by increasing the average power. However, the dimensional accuracy was found to be negatively affected by the increased exposure time. Pulsed SLM systems give more flexibility to control the volumetric energy density for denser and higher hardness compared to continuous wave SLM systems as it was shown with Al-12Si alloys [6]. Moreover, pulsed-SLM systems improved the surface roughness and are suitable for lattice structures and thin walls [5,7]. Even though the pulsed laser systems deliver lower average power than continuous systems, they result in stronger sintering connection between grains [8].

Volumetric energy density (VED) is the amount of energy applied to a unit volume of powder. However, variation in part densities may be caused by the combination of parameters that deliver

Contents lists available at ScienceDirect

## Additive Manufacturing

j o u rn al hom ep

age: www.elsevier.com/locate/addma

<!-- image -->

<!-- image -->

LT

Fig. 1. Different particle size distributions (PSD) vs. fixed layer thickness (LT).

<!-- image -->

the VED. For instance, using a hatching distance of 100 𝛍 m with a scan speed of 50 mm/s gives the same VED as using a hatching distance of 50 𝛍 m and a scan speed of 100 mm/s but the resulting part density is different. When the hatching distance is large, there will be no overlap between adjacent lines. The melt pool size increases when the laser power is high and scan speed is slow. If the distance between scan lines is larger than the melt pool size, voids (unmolten powder) will be created [9,10]. The relationship between part density and VED is not linear, and there are ranges of process parameters that can be used to fabricate near full density parts. This means that the value of VED should not be used as an appropriate indicator of melt energy for obtaining parts with defined density.

Process parameters are not the only factors that affect the quality of SLM parts. Powder properties such as particle size distribution (PSD) also influence the density of the part produced at a certain VED. Simchi [11] found that for a given layer thickness, using a smaller particle size distribution gives increased density until a specific point is reached. However, they showed that below this point, using smaller powder particle can negatively affect the density. This could be due to the amount of powder vs layer thickness. Heat transfer from the top layer to the bottom is affected by the number and size of the gaps between the particles, together with the thermal conductivity of powder. Fig. 1 illustrates the potential differences between the amount and the size of gaps for different particle size distributions for a given layer thickness. Therefore, it is possible that insufficient melt energy reaches the bottom of the layer leaving un-melted powder [12]. Additionally, smaller particles sizes have a greater potential to be disturbed by the high energy of the laser, therefore creating voids in the distributed layer.

The effect of particle size distribution (PSD) on the SLM process and on the fabricated parts has been studied for 316L [13,14] and Ti64 [15]. The results of these studies can be summarised as follows: metallic powder that has a small PSD (more fine particles [13]) tends to have denser powder bed and higher thermal conductivity. These two characteristics help to fabricate parts with higher density, smoother surfaces and higher mechanical strength compared to parts fabricated by coarse/large particles powder. However, a large proportion of fine particles may lock together causing poor flow. On the other hand, powder with large PSD has better flowability and parts that are fabricated by larger particle size have higher elongation.

Spierings and Levy [4] found that the actual layer thickness is different to the theoretical layer thickness and can be described as the effective layer thickness ( LT eff ). The effective layer thickness can be calculated according to the density of layer thickness using the following equation, Eq. (1):

<!-- formula-not-decoded -->

Table 1 Particle size distributions and density of all powder types: T1, T2 and T3.

|                            | Ti64 Powder Type   | Ti64 Powder Type   |      |
|----------------------------|--------------------|--------------------|------|
|                            | T1                 | T2                 | T3   |
| D10 ( 𝛍 m)                 | 20.6               | 43.2               | 51.7 |
| D50 ( 𝛍 m)                 | 32                 | 59.3               | 73.6 |
| D90 ( 𝛍 m)                 | 48.6               | 81.2               | 105  |
| Powder Density (g/cm 3 )   | 4.42               | 4.41               | 4.41 |
| Apparent Density (g/cm 3 ) | 2.58               | 2.60               | 2.50 |
| Tapped Density (g/cm 3 )   | 2.86               | 2.85               | 2.78 |

Where; Dm is the density after melting, Dp is the density of the powder layer and LT is the theoretical layer thickness. Therefore, the actual layer thickness that is affected by melting energy is the effective layer thickness which should be considered when selecting the process parameters.

A review of previous work suggests that little work has been carried out on the correlation of particle size and layer thickness and their effect on the density of fabricated parts, specifically for pulsed SLM systems. This work addresses this gap in existing knowledge and aims to determine the influence of changing powder size and layer thickness for the same volumetric energy density which is controlled by exposure time.

## 2. Materials and methods

The study carried out comprised two main phases. The first phase comprised a process parameter optimisation. A single powder type was used for optimisation to find the most influential parameters and determine the best combination to achieve the highest part density. The design and analysis of experiments were carried out using the Taguchi experimental design method. In the second phase, three types of powder with different particle size distributions (PSD) were used to investigate the effect of PSD and layer thickness on part density where other process parameters were fixed at their optimum values.

## 2.1. Materials selection and processing conditions

Three types of Titanium alloy Ti6Al4V ELI powder with different particle size distributions (PSD) were used in this research. The powders are gas-atomised and are spherical in their nature. Their particle size distributions and density are shown in Table 1.

Table 2 shows the nominal chemical analysis which reveals low oxygen content (approximately 0.1 wt%). The laser melting machine is an AM250 model, manufactured by Renishaw in the UK, and equipped with a 200W modulated fibre laser which generates a pulsed laser wave. The laser beam has a minimum nominal diameter of 70 𝛍 m and wavelength of 1070 nm. The machine has a build volume of 250 mm x 250 mm x 300 mm. The spot size of the beam was kept at its minimum value for all builds for providing the high-

Table 2 Chemical composition of all powder types: T1, T2 and T3 in weight percentage (wt%).

| Powder Type   |   AL |    V |     O | N      |     C | H      |    Fe | Ti   |
|---------------|------|------|-------|--------|-------|--------|-------|------|
| T1            | 6.5  | 3.9  | 0.11  | 0.03   | 0.01  | <0.01  | 0.2   | Bal. |
| T2            | 6.14 | 4.14 | 0.086 | <0.005 | 0.013 | 0.0012 | 0.05  | Bal. |
| T3            | 6.16 | 4.17 | 0.08  | <0.005 | 0.012 | 0.0012 | 0.049 | Bal. |

est possible energy density, as recommended by the manufacturer profile.

In the optimisation phase, laser power (P), scan speed (SS) and hatching distance (HD) were considered to be the most critical parameters. In pulsed SLM systems, the laser does not fire continuously but rather in a discrete manner. In this case the scan speed is calculated according to point distance (PD, the distance between two consecutive points), exposure time (ET, the elapsed time for each laser beam firing), and jump speed (JS, the speed the mirrors move when the laser moves from point to point). Eq. (2) was used to calculate the scan speed.

<!-- formula-not-decoded -->

In this study the jump speed was kept at 5000 mm/s for all builds. The parameters and their selected levels are shown in Table 3. In pulsed SLM, however, it is not accurate to study the effect of scan speed as a single parameter on part quality. The scan speed can be obtained by different parameter combinations, but not all are suitable for use even when the combined values are identical. For instance, using a combination of a PD of 50 𝛍 m and an ET of 50 𝛍 s will lead to the same scan speed as a PD of 200 𝛍 m and an ET of 200 𝛍 s. Even though the value of scan speed is exactly the same, the later combination may not be suitable for full density builds, as the size of melt pool will not cover the distance between consecutive points (PD) even with the longer firing time (ET). Therefore, each individual parameter must be carefully selected.

Process parameter optimisation was carried out using powder type 1 (T1). The build platform was pre-heated up to 170 ◦ C in line with the standard build procedure recommended by the manufacturer, and all builds were fabricated under Argon atmosphere with oxygen level below 0.1%.

In the second phase, the process parameters found in the optimisation phase were used with different PSDs to study the effect of changing powder and layer thickness on part density when other parameters were fixed. However, keeping the parameters that are found to be optimum for a specific PSD powder may not be optimum for other PSD powders. Spierings et al., when selective laser melting steel parts, successfully used fixed parameters with a changing PSD when studying the effect on part density [4], surface finish and mechanical properties [14]. In both studies the scan speed and layer thickness were varied to produce a range of energy densities that was applied to powders of different PSDs. Liu et al. [13] also used fixed parameters when investigating the effect of PSDs on process parameter optimisation. Spot diameter and scanning speed were varied while other parameters kept constant for different PSD powders.

Table 3 Process parameters and their levels used in the experiments.

| Parameter                      |   Levels |   Levels |   Levels |   Levels |   Levels |
|--------------------------------|----------|----------|----------|----------|----------|
|                                |        1 |        2 |        3 |        4 |        5 |
| Layer Thickness, LT - ( 𝛍 m)   |       20 |       30 |       50 |       70 |      100 |
| Laser Power, LP - (W)          |       90 |      120 |      150 |      180 |      200 |
| Point Distance, PD - ( 𝛍 m)    |       35 |       45 |       55 |       70 |      100 |
| Exposure Time, ET ( 𝛍 s)       |       50 |       70 |      100 |      150 |      200 |
| Hatching Distance, HD - ( 𝛍 m) |       50 |       60 |       70 |       85 |      100 |

Table 4 Exposure time range and number of samples for each layer thickness.

| LT ( 𝛍 m)               | 60     | 80     | 100    |
|-------------------------|--------|--------|--------|
| ET range ( 𝛍 s)         | 40-250 | 60-330 | 70-420 |
| Number of samples       | 22     | 28     | 36     |
| Repeat                  | 4      | 4      | 4      |
| Total number of samples | 88     | 112    | 144    |
| Total                   | 344    |        |        |

In this study, all process parameters, except layer thickness and exposure time, were kept constant using the optimum values determined during the first phase. Each powder type was used to build parts with layer thicknesses of 60, 80 and 100 𝛍 m. The exposure time was varied in increments of 10 𝛍 s to study its effect on layer thickness for a particular PSD. Table 4 shows the layer thicknesses and exposure time values.

The range of volumetric energy density (Eq. (3)) was approximately the same for all layer thicknesses. For each powder type, 344 samples were produced, resulting in a total, for this phase, of 1032 samples.

<!-- formula-not-decoded -->

The same value of VED can be obtained from different process parameter combinations. However, some combinations may not be suitable for a successful build.

## 2.2. Design of experiments and Taguchi method

The Taguchi approach is one of the most powerful and reliable evaluating methods used in multi-factor experiments. It has been used to investigate the main effects of design parameters with the fewest number of experiments [16]. The method has previously been used to optimise process parameters in SLM [17] and in Laser Engineering Net Shaping [18]. In principle, Taguchi's design of experiments is used to obtain information about the main effects of the input factors. The objectives of the Taguchi approach for parameter design are to find out the best combination of design parameters and reduce the variation of the response. The Signalto-Noise (S/N) ratio is the analysis characteristic that underpins the Taguchi method. The main aim for these experiments is to optimise the laser process parameters to obtain higher density. Therefore, the S/N ratio was calculated using the following equation (Eq. (4)):

<!-- formula-not-decoded -->

where y is the observed data and n is the number of observations.

Thus, for five five-level factors there are a total of 5 5 = 3125 different combinations that should be considered for full factorial design. Using other fractional design such as Central Composite Design (CCD) and Box-Behnken Design (BBD) leads to 52-104 and 46-60 combinations (experiments) respectively. The range of the number of experiments of CCD and BBD depends on the number of factors that are considered as continuous or categorical factors. However, using the Taguchi approach for designing the experiments, the number of attempts required can be reduced to save time and resources and the approach still yields results in good agreement with other methods [19]. According to the Taguchi approach, the samples can be organized into only 25 groups. An orthogonal array of L25 was used for 5 parameters and 5 levels. Each run was repeated four times. Minitab17 was used to build and analyse the experimental design.

102.5

74

100.0-

T

95.0

Relative Density %

T1

Fig. 2. Samples labelling and arrangement on the build platform.

<!-- image -->

## 2.3. SLM builds

The samples selected were 10 × 10 × 10 mm 3 cubes with 3 mm supports. Each was labelled with a unique identification number. There were four cubes for each process parameter combination for all experimental builds, arranged on the platform alternately to mitigate the effect of particles rejected from the melt pool during the process of neighbouring cubes (see Fig. 2)

In the next phase, the process parameters were optimised then used with different powders with a different particle size distribution (PSD) to investigate the effect of changing layer thickness (LT) on part density. A variable ET was used to keep the VED constant and study its effect on the density of samples when LT and PSD were changed.

## 2.4. Porosity characterization

The density of the samples was measured using the Archimedes principle which is considered by Spierings et al. [20] to be a reliable and fast method. As the build supports were processed using a different melt strategy from the selected melt parameters, the samples were ground to remove any residual supports insuring that the samples evaluated are purely built by the selected strategy. After support removal, the samples were ultrasonically washed using

Table 5 Response Table for Signal to Noise Ratios (Larger is better) for resultant density.

|       | S/N for factor:   | S/N for factor:   |       |       |       |
|-------|-------------------|-------------------|-------|-------|-------|
| Level | LT                | LP                | PD    | ET    | HD    |
| 1     | 12.87             | 12.64             | 12.76 | 12.71 | 12.75 |
| 2     | 12.87             | 12.72             | 12.76 | 12.7  | 12.85 |
| 3     | 12.67             | 12.74             | 12.87 | 12.81 | 12.69 |
| 4     | 12.64             | 12.79             | 12.61 | 12.7  | 12.8  |
| 5     | 12.66             | 12.81             | 12.71 | 12.79 | 12.61 |
| Delta | 0.23              | 0.17              | 0.26  | 0.11  | 0.24  |
| Rank  | 3                 | 4                 | 1     | 5     | 2     |

2425

Ultraclean SA solution with water (5:100 ml) for 15 min in 45 ◦ C to remove any residual powder. The density of the samples were evaluated using Archimedes method [21]. The densities of the parts were analysed using Minitab17 to establish the significant factors that affect the density of SLM fabricated samples and therefore the best determine combination of parameters to give highest density.

## 3. Results and discussion

## 3.1. Density

The optimisation experimental results are illustrated in Fig. 3, where the maximum average relative density (ARD) is 99.97% for run number 6. The accuracy of measurements using the selected method depends on the surface roughness and the surface tension of the liquid. When the surface is smooth, the variation of the measurements is small and vice versa.

To find the most effective parameters in this study, the S/N ratio was analysed and summarised in Table 5. Delta in the table shows the difference between maximum and minimum S/N ratio of the levels of each factor. The value of Delta represents the significance of a factor, the higher the Delta, the more significant the factor.

Higher values of the signal-to-noise ratio (S/N) identify control factor settings that minimise the effects of the noise factors. The factors are ranked according to their effectiveness. As shown in Table 5 and Fig. 4, PD and HD are the most significant factors, Rank 1 and Rank 2 respectively. Layer thickness is the third most influential factor on the process, followed by laser power (LP) and finally, exposure time (ET).

Fig. 3. The measurements accuracy of the density of the cubes in each run.

<!-- image -->

T1

T1

6

Mean of SN ratios

12.90

12.85

12.80

12.75

12.70-

12.65-

12.60

20 30 50 70 100 90 120 150 180 200 35 45 55 70 100 50 70 100 150 200 50 60 70 85 100

Signal-to-noise: Larger is better

Table 6 Validation process parameters

levels.

Table 7 Comparison results of the process parameter combinations found by Taguchi validation experiments against manufacturer profile.

|   # | Parameter                  |   Levels |    |    |    |     |    |
|-----|----------------------------|----------|----|----|----|-----|----|
|   1 | Layer Thickness - ( 𝛍 m)   |       30 |    |    |    |     |    |
|   2 | Laser Power - (W)          |      200 |    |    |    |     |    |
|   3 | Point Distance - ( 𝛍 m)    |       50 | 55 |    | 60 |     | 65 |
|   4 | Exposure Time ( 𝛍 s)       |       50 |    | 90 |    | 100 |    |
|   5 | Hatching Distance - ( 𝛍 m) |       55 |    | 60 |    |  65 |    |

and

| Parameter                  |   Taguchi |   Valid. Process 1 |   Valid. Process 2 |   Manufacturer profile |
|----------------------------|-----------|--------------------|--------------------|------------------------|
| Layer Thickness - ( 𝛍 m)   |     30    |              30    |              30    |                  30    |
| Laser Power - (W)          |    200    |             200    |             200    |                 200    |
| Point Distance - ( 𝛍 m)    |     55    |              50    |              65    |                  75    |
| Exposure Time ( 𝛍 s)       |    100    |              50    |              50    |                  50    |
| Hatching Distance - ( 𝛍 m) |     60    |              65    |              65    |                  65    |
| Relative Density%          |     99.62 |              99.83 |              99.72 |                  99.53 |

The optimal parameter combination from the selected experimental design is: layer thickness of 30 𝛍 m, laser power of 200 W (maximum power gives greater flexibility in choosing other parameter ranges [22]), the distance between points of 55 𝛍 m, exposure time of 100 𝛍 s, and hatching distance of 60 𝛍 m.

Validation experiments were carried out using the same materials and equipment as previously described. The levels of factors were chosen around the best combination parameters that were established by the Taguchi method. Layer thickness and laser power were fixed at 30 𝛍 m and 200W respectively. The experiments were run as full factorial experiment (see Table 6).

The results of the validation experiments show that there are other values of point distance and hatching distance that can give higher part density. Two other combinations of process parameters were obtained: the first where PD is 50 𝛍 m, ET is 50 𝛍 s, and HD is 65 𝛍 m and the second where PD, ET, and HD are 65 𝛍 m, 50 𝛍 s, and 65 𝛍 m respectively. From the comparison table, Table 7, the density of the parts that were fabricated using the new parameters combinations, found by validation experiments, is higher than the density that was obtained by either the Taguchi method or the manufacturer recommendation. Using the exposure time suggested by Taguchi, ET of 100 𝛍 s, keeps the process robust and less sensitive

LT

Main Effects Plot for SN ratios

Data Means

LP

PD

ET

HD

Fig. 4. Main effects plots for S/N ratios (larger is better) for the resultant density.

<!-- image -->

to the slight changes in other parameters such as PD and HD. It should be noted that the density is compared against the theoretical density of the alloy.

Fig. 5 shows the relationship between VED and relative density for each layer thickness. The results show that it is possible to fabricate parts with a higher layer thickness and still obtain high density.

Using a layer thickness of 30 𝛍 m gives the highest relative density. It is, however, possible to use thicker layer thicknesses with suitable VEDs in the optimal parameter window to fabricate high density parts, as all layer thicknesses achieved a relative density of approximately 99%.

The noticeable variation in density for a single layer thickness might be caused by a combination of parameters, not only by the value of VED. For the second and third points of the 70 𝛍 m layer thickness in Fig. 5, it can be noted that the combination of process parameters led to similar VED values, however, the part densities varied. The main effect in this case was the point distance (PD). The third point has double the point distance of the second point, 100 vs 55 𝛍 m respectively and the density of the third point is 97% while the second point has a density of 99%. It is clear from above that the VED is not a single value that can be applied to achieve a successful build and that it is important to understand the combination of parameters that deliver a specific value of VED. Therefore, the values of process parameters should be carefully selected to establish certain values of scan speed or VED. Fig. 6 shows that there is a linear relationship between LT and RD, and also LP and RD but the other three factors exhibit non-linear relationship with RD.

## 3.2. LT and PSD vs ET

From the results in Table 7, the process parameters of LP of 200, PD of 50, and HD of 65 were selected to investigate the effect of changing layer thickness and powder size distribution on the density of parts at different exposure times. Three powder types T1, T2 and T3 were used to build 10 × 10 × 10 mm 3 cubes with layer thicknesses of 60, 80 and 100 𝛍 m. The exposure time was varied according to layer thickness.

Fig. 7 shows the correlation between ET and relative density for each powder type and layer thickness builds. Generally, using large particles or thicker powder layers decreases part density, yet it is possible to obtain 99% relative density using any of these powder types. As the ET increases (VED increases) the part density increases

100

101

99

100

98

Relative density

97

99

96

98

95

97

94

96-

93

92

91

All displayed terms are in the model.

90

0.00

·

60

50.00

Relative density vs. VED

Main Effects Plot for RD

PD

<!-- image -->

100.00

Fig. 5. Relative density versus VED for each layer thickness obtained from optimisation phase.

Fig. 6. Main effects plot for relative density (RD) and its relationship with each parameter.

<!-- image -->

until a specific level. Beyond that level the density did not improve even with increased exposure time.

Plots (a-c) are for powder type T1, plots (d-f) are for powder type T2 and plots (g-i) are for powder type T3. Each plot is identified by the powder type and its layer thickness (e.g. T2-80 is the plot of powder type T2 and layer thickness 80 𝛍 m). The VED in plot a, b and c at exposure time of 40, 60 and 70 respectively are almost the same. However, this VED led to different relative densities, approximately 97% for T1-60, 99% for T1-80 and 98.5% for T1-100.

The plots (d) and (g) look very similar because the particle size that fits into their layer thicknesses is almost identical. By assuming that the powder layer density was between the apparent density and the tapped density [23,24], a value of 60% was used. This means the effective layer thickness of LT 60 𝛍 m would be approximately 84 𝛍 m (according to Eq. (1)). Thus, powder particles of powder types T2 and T3 that can be packed in layer thickness of 84 𝛍 m will be from 27.4 to 84 𝛍 m and from 31.1 to 84 𝛍 m respectively. As a result, it is expected that these ranges of powder particles would lead to the same, or similar, results.

Even though the exposure time of 40 𝛍 s and a layer thickness of 60 𝛍 m provides a higher VED than an ET of 70 𝛍 s and an LT of 100 𝛍 m, the RD of the later was higher (above 98.5%). This confirms that the VED is not an accurate indicator to select a suitable energy for fully melting powder; each factor should be taken into consideration, especially for pulsed SLM.

## 3.3. Part location effects

For 15 builds (1032 samples), the part location on platform was analysed to establish the optimum location on the platform for the highest part density. The colour map in Fig. 8 shows that the parts built in the top right of the platform have the potential for higher densities compared with those built elsewhere on the platform but using the same process parameters.

The illustration bars represent the normalised porosity variation. They can be considered as indicators of the probability of obtaining lower density builds when compared to other locations on the platform. For Fig. 8(a) and (b), it is assumed that the origin of the platform is located in the bottom left corner, as the machine coordinate system is defined in [25]. X-axis and Y-axis values are the distance from the origin. Fig. 8(a) shows that the analysis of part location covered a 200 × 200 mm 2 area starting 20 mm from the origin on X and Y. The analysed area was reduced in (b) to cover an area of 150 × 150 mm 2 starting 50 mm from the origin on X and Y. There are many possible reasons that may cause the variation in density when building in different locations such as:

90

ET

HD

100.0

99.5

99.0

98.5

98.0

220

97.5

97.0

170

120

100

99

70

98

97

20

96-

95

94

93

100

99

98

97

96

95

94

93

п 506 8,00

Fitted Line Plot (T1-60)

RD = - 95.80 + 284.4 log10(ET)

- 137.1 log10(ET)^2 + 21.89 log10(ET)^3

Regression

95% PI

95% CI

100.0

95% CI

Fitted Line Plot (T1-100)

RD = 4.27 + 130.9 log10(ET)

- 59.93 log10(ET) ^2 + 9.102 log10(ET)^3

Regression

95% PI

95% CI

Fig. 7. Fitted lines of the relative density (RD) with respect to exposure time (ET) for all powder types: T1; T2; T3 and layer thicknesses (LT): 60; 80; 100.

<!-- image -->

Fig. 8. Colour map of the potential best build location on the platform where the blue colour represents the location where the potential porosity is minimal. (For interpretation of the references to colour in this figure legend, the reader is referred to the web version of this article.)

<!-- image -->

- Wiping powder direction
- Rejected powder particles from melt pool [26,28]
- Gas pressure flow direction [26-28]
- Laser beam deformation (focus) when the beam is at an extreme angle
- Number of parts on the platform

The results suggest that part location can have negative influence on part quality for the current generation of machine design.

However, it is secondary compared to the influence of process parameter selection.

## 4. Conclusion

In this study, the effect of particle size distribution and layer thickness on part density was studied. It was found that the density of parts is not only affected by the applied VED), but also by the parameters that deliver the VED. In other words, the same VED value can be obtained by different configurations of parameters,

Wiping Powder

20

- 200.7 log10(ET) ^ 2 + 30.64 log10(ET)^ 3

2

Fitted Line Plot (T1-80)

RD = 22.32 + 109.7 log10(ET)

- 51.95 log10(ET) ^2 + 8.158 log10(ET)^3

95% PI

99.5

but the results may be completely different. The most significant factors that affect the process are distance between points (PD) and hatching distance (HD), which control melt overlapping. The best combination of parameters for high density parts was a PD of 50 𝛍 m, HD of 65 𝛍 m, LT of 30 𝛍 m, LP of 200 W, and ET of 50 𝛍 s. This combination of parameters resulted in 100% relative density and sample properties that compared well with wrought material properties. In addition, it was found that it is possible to produce a near fully dense part with thicker build layers by selecting a suitable VED. A density of approximately 99% was obtained for all layer thicknesses. However, using a thinner layer leads to higher density at lower VED than using a thicker layer. Similarly, using small powder particles helps achieve higher density in a considerably shorter production time. From all types of powder and layer thicknesses, it was observed that exposure time in this SLM system should not be lower than 50 𝛍 s even for small powder particles and thin powder layers. Finally, part location on the platform leads to a slight different part density due to machine architecture and process behaviour.

## Acknowledgement

I acknowledge the support of King Saud University, Riyadh, Saudi Arabia.

## References

- [1] W.E. Frazier, Metal additive manufacturing: a review, J. Mater. Eng. Perform. 23 (2014) 1917-1928, http://dx.doi.org/10.1007/s11665-014-0958-z.
- [2] D.D. Gu, W. Meiners, K. Wissenbach, R. Poprawe, Laser additive manufacturing of metallic components: materials, processes and mechanisms, Int. Mater. Rev. 57 (2012) 133-164, http://dx.doi.org/10.1179/ 1743280411Y.0000000014.
- [3] E. Herderick, Additive manufacturing of metals: a review, Mater. Sci. Technol. Conf. Exhib. (2011) 1413-1425, MS T'11. 2 (2011) http://www.scopus.com/ inward/record.url?eid=2-s2.0-
4. 84856301323&amp;partnerID=40&amp;md5=e02018d10b2ca37a7e2ae1773e4fcaec. [4] A.B. Spierings, G. Levy, Comparison of Density of Stainless Steel 316L Parts Produced with Selective Laser Melting Using Different Powder Grades, in: Annu. Int. Solid Free. Fabr. Symp. Univ., Texas, Austin, TX, USA, 2009 (p. 20).
- [5] A.G. Demir, P. Colombo, B. Previtali, From pulsed to continuous wave emission in SLM with contemporary fiber laser sources: effect of temporal and spatial pulse overlap in part quality, Int. J. Adv. Manuf. Technol. 91 (2017) 2701-2714, http://dx.doi.org/10.1007/s00170-016-9948-7.
- [6] R. Chou, J. Milligan, M. Paliwal, M. Brochu, Additive manufacturing of Al-12Si alloy via pulsed selective laser melting, JOM 67 (2015) 590-596, http://dx.doi. org/10.1007/s11837-014-1272-9.
- [7] K.A. Mumtaz, N. Hopkinson, Selective Laser Melting of thin wall parts using pulse shaping, J. Mater. Process. Technol. 210 (2010) 279-287, http://dx.doi. org/10.1016/j.jmatprotec.2009.09.011.
- [8] P. Fischer, V. Romano, H.P. Weber, S. Kolossov, Pulsed laser sintering of metallic powders, Thin Solid Films 453-454 (2004) 139-144, http://dx.doi. org/10.1016/j.tsf.2003.11.152.
- [9] L.S. Bertol, W.K. Júnior, F.P. Da Silva, C. Aumund-Kopp, Medical design: direct metal laser sintering of Ti-6Al-4V, Mater. Des. 31 (2010) 3982-3988, http:// dx.doi.org/10.1016/j.matdes.2010.02.050.
- [10] H. Gong, K. Rafi, T. Starr, B. Stucker, The effects of processing parameters on defect regularity in Ti-6Al-4V parts fabricated by selective laser melting and electron beam melting, 24th Annu. Int. Solid Free. Fabr. Symp. (2013), pp. 424-439.
- [11] A. Simchi, Direct laser sintering of metal powders: mechanism, kinetics and microstructural features, Mater. Sci. Eng. A 428 (2006) 148-158, http://dx.doi. org/10.1016/j.msea.2006.04.117.
- [12] C. Boley, S. Khairallah, A.M. Rubenchik, Modeling of powder absorption in additive manufacturing, in: 25th Annu. Int. Solid Free. Fabr. Symp., Auston, TX, USA, 2014, http://dx.doi.org/10.1364/CLEO AT.2014.AM1L.5 (p. AM1L.5).
- [13] B. Liu, R. Wildman, C. Tuck, I. Ashcroft, R. Hague, Investigation the effect of particle size distribution on processing parameters optimisation in selective laser melting process, SFF (2011) 227-238.
- [14] A.B. Spierings, N. Herres, G. Levy, Influence of the particle size distribution on surface quality and mechanical properties in AM steel parts, Rapid Prototyp. J. 17 (2011) 195-202, http://dx.doi.org/10.1108/13552541111124770.
- [15] A. Hicks, H. Doak, B. Stucker, Effects of powder variation on the microstructure and tensile strength of Ti6Al4V parts fabricated by selective laser melting, solid free, Fabr. Symp. (2014) 470-483.
- [16] Phillip J. Ross, Taguchi Techniques for Quality Engineering, 2nd ed., McGraw Hill Professional, New York, 1996.
- [17] J. Sun, Y. Yang, D. Wang, Parametric optimization of selective laser melting for forming Ti6Al4V samples by Taguchi method, Opt. Laser Technol. 49 (2013) 118-124, http://dx.doi.org/10.1016/j.optlastec.2012.12.002.
- [18] C.P. Paul, P. Ganesh, S.K. Mishra, P. Bhargava, J. Negi, A.K. Nath, Investigating laser rapid manufacturing for Inconel-625 components, Opt. Laser Technol. 39 (2007) 800-805, http://dx.doi.org/10.1016/j.optlastec.2006.01.008.
- [19] A. Asghar, A.A. Abdul Raman, W.M.A.W. Daud, A comparison of central composite design and Taguchi method for optimizing Fenton process, Sci. World J. 2014 (2014) 869120, http://dx.doi.org/10.1155/2014/869120.
- [20] A.B. Spierings, M. Schneider, R. Eggenberger, Comparison of density measurement techniques for additive manufactured metallic parts, Rapid Prototyp. J. 17 (2011) 380-386, http://dx.doi.org/10.1108/ 13552541111156504.
- [21] STM B-311, Standard Test Method for Density of Powder Metallurgy (PM) Materials Containing Less Than Two Percent Porosity 1, ASTM Int., West Conshohocken, 2008, pp. 1-5, http://dx.doi.org/10.1520/B0311-13.2.
- [22] C. Kamath, B. El-dasher, G.F. Gallegos, W.E. King, A. Sisto, Density of additively-manufactured, 316L SS parts using laser powder-bed fusion at powers up to 400 W, Int. J. Adv. Manuf. Technol. (2014) 65-78, http://dx.doi. org/10.1007/s00170-014-5954-9.
- [23] Y. Bai, G. Wagner, C.B. Williams, Effect of bimodal powder mixture on powder packing density and sintered density in binder jetting of metals, 2015 Annu. Int. Solid Free. Fabr. Symp. (2015) 62, http://dx.doi.org/10.1017/ CBO9781107415324.004.
- [24] E.O. Olakanmi, Selective laser sintering/melting (SLS/SLM) of pure Al, Al-Mg, and Al-Si powders: effect of processing conditions and powder properties, J. Mater. Process. Technol. 213 (2013) 1387-1405, http://dx.doi.org/10.1016/j. jmatprotec.2013.03.009.
- [25] ISO/ASTM 52900:2015(E), Standard Terminology for Additive Manufacturing -General Principles -Terminology, ISO/ASTM 52900, ISO/ASTM 5, 2015, pp. 1-9, http://dx.doi.org/10.1520/F2792-12A.2.
- [26] M.J. Matthews, G. Guss, S.A. Khairallah, A.M. Rubenchik, P.J. Depond, W.E. King, Denudation of metal powder layers in laser powder bed fusion processes, Acta Mater. 114 (2016) 33-42, http://dx.doi.org/10.1016/j.actamat. 2016.05.017.
- [27] B. Ferrar, L. Mullen, E. Jones, R. Stamp, C.J. Sutcliffe, Gas flow effects on selective laser melting (SLM) manufacturing performance, J. Mater. Process. Technol. 212 (2012) 355-364, http://dx.doi.org/10.1016/j.jmatprotec.2011. 09.020.
- [28] A. Ladewig, G. Schlick, M. Fisser, V. Schulze, U. Glatzel, Influence of the shielding gas flow on the removal of process by-products in the selective laser melting process, Addit. Manuf. 10 (2016) 1-9, http://dx.doi.org/10.1016/j. addma.2016.01.004.