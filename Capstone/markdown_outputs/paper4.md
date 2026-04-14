<!-- image -->

Contents lists available at ScienceDirect

## Additive Manufacturing

journal homepage: www.elsevier.com/locate/addma

## Residual stress evaluation in selective-laser-melting additively manufactured titanium (Ti-6Al-4V) and inconel 718 using the contour method and numerical simulation

Bilal Ahmad a, ⁎ , Sjoerd O. van der Veen b , Michael E. Fitzpatrick a , Hua Guo a

- a Faculty of Engineering, Environment and Computing, Coventry University, Gulson Road, Coventry, CV1 2JH, UK

b Airbus Operations SAS, 316 route de Bayonne, Toulouse, France

## A R T I C L E I N F O

Keywords: Selective laser melting Additive manufacturing Residual stress Inherent strain-based method Contour method

## 1. Introduction

Selective laser melting (SLM) is a form of powder-bed fusion additive manufacturing [1]. It works by melting and bonding successive layers of powder metal to produce three-dimensional shapes with the use of a high-power laser [2]. The process usually takes place under an inert gas. Computer-Aided Design (CAD) software is used in the SLM process, which converts the full three-dimensional geometry to a series of layers for each laser pass. The thickness of each layer and a tool path are also de fi ned [1]. A variety of complex and small shapes can be produced with SLM. The surface fi nish of parts built with SLM is generally better than other additive manufacturing processes [3].

Titanium (Ti-6Al-4V) and Inconel 718 alloys both fi nd applications with the aerospace industry. The cost of these materials is high, and conventional machining of parts can have high rates of scrap materials produced, hence SLM provides a cost-e ff ective solution due to little material wastage and less or no fi nal machining required.

Selective laser melting is known to generate tensile residual stresses during the build process [4 -6]. During the SLM process a large amount of heat is produced which causes thermal gradients in the components [7]. Shrinkage during SLM additive manufacturing is the main cause of generation of residual stress, which is similar to the case for fusion welds. The layer-by-layer build-up changes the original tensile residual

⁎ Corresponding author.

E-mail addresses: ac2333@coventry.ac.uk (B. Ahmad), sjoerd.van-der-veen@airbus.com (S.O. van der Veen), michael. fi tzpatrick@coventry.ac.uk (M.E. Fitzpatrick),

## A B S T R A C T

Residual stresses play an important role for the structural integrity of engineering components. In this study residual stresses were determined in titanium alloy (Ti-6Al-4V) and Inconel 718 samples produced using selective-laser-melting (SLM) additive manufacturing. The contour method and a numerical simulation approach (inherent-strain-based method) were used to determine the residual stress distributions. The inherent-strainbased method reduces the computational time compared to weakly-coupled thermo-mechanical simulations. Results showed the presence of high tensile residual stresses at and near the surface of both titanium and Inconel alloys samples, whereas compressive residual stresses were seen at the center region. A good agreement was seen between the results obtained from contour method and the numerical simulation, particularly 1 mm below the surface of the samples.

stress to compressive. The shrinkage in SLM additive manufacturing is considered to be anisotropic due to the fast cooling rate [8]. As a result of this the residual stress distribution in the top surface layer is not uniform [9]. The top surface layer ends up with tensile residual stress and compressive residual stress below it [7].

Numerical simulation [10,11] as well as experimental techniques [5,6,12,13] have been used to characterize residual stress in SLM parts. For example, residual stresses in metal SLM have been previously characterized in austenitic stainless steel AISI 316L using X-ray diffraction [13]. Digital image correlation has also been used to measure residual stresses [14]. Thermo-mechanical numerical prediction showed tensile residual stresses approaching 300 MPa in the top layer of a cantilever sample along its length direction, which were signi fi cantly reduced after removing the sample from the base plate [10]. A thermo-mechanical numerical prediction of AlSi10Mg over a few micro-seconds duration during the build process showed relatively high compressive residual stress (about -80 MPa) at the sample inner surface which decreased towards the edges (reaching about -38 MPa) [15]. A small tensile residual stress was also predicted at the start and end locations of the printing [15]. High tensile residual stress approaching 600 MPa was predicted in the top layer of an SLM steel sample [16]. A good correlation has been reported between the residual stresses obtained from the contour method and neutron di ff raction for

<!-- image -->

<!-- image -->

Location of cut

→

Fig. 1. Principle of residual stress measurement with contour method.

<!-- image -->

laser-direct-metal deposited Waspaloy [12].

Coupled thermo-mechanical fi nite element simulation has successfully been used to predict the phenomena of di ff erential shrinkage and generation of residual stress. A summary of the relevant literature can be found in [17]. The problem with even weakly-coupled thermo-mechanical simulations is the long run-time. In spite of all the progress in fi nite element solver technology and hardware, it still takes more than one night to come to a prediction of residual stress in an industrial-size powder-bed part. In the present work it was therefore decided to sacri fi ce modelling fi delity in exchange for solving speed, by using an inherent-strain-based method to simulate metal SLM. The use of inherent strain to analyze residual stress in welded structures was fi rst described in [18] and successfully applied to various cases thereafter [19,20]. The inherent strain method originally is a method to measure three-dimensional residual stresses. The inherent strain is de fi ned as an incompatible strain in a body producing residual stress. Inherent strain may contain strains from various sources such as thermal and plastic strain [20]. This method allows dividing the three-dimensional inherent strains to longitudinal and traverse components (e.g. for welds). The stresses for both components are then analyzed separately, and by adding both components it allows estimation of three-dimensional stresses [19].

Metal SLM di ff ers from those conventional welding cases by the large number of passes made by a highly focalized heat-source, to build up a generally very complex shape (such as highly optimized ' bird skeleton ' designs). A true steady-state welding condition is therefore not always achieved and it can be anticipated that the inherent strain fi eld in such a part is highly inhomogeneous. This has been illustrated in the pure eigenstrain -approach reported in [21]. Generally eigenstrain is considered as a permanent strain in a material developed due to phase transformation, thermal expansion, and plastic deformation [22]. The eigenstrain theory accounts for the eigenstrain in material and calculates the resulting residual stresses. In the present paper, the inherent strain is de fi ned as the strain resulting from the material-process combination in steady-state conditions, like in a classical metal weld at some distance from the start and the end points. It represents the material-process combination at the weld-pool scale. The term eigenstrain , on the other hand, is used in [21] for the more general mathematical construct of Mura [22] and especially Korsunsky [23]. It allows application of a strain fi eld to a continuum to reproduce an arbitrary stress fi eld.

Previous research [21] highlights the di ffi culty of reconstructing an eigenstrain fi eld that can predict both residual stress and part distortion in SLM. On the other hand, the inherent-strain-based method greatly reduces the computational e ff ort compared to even weakly-coupled thermo-mechanical simulations, hence the choice of the inherentstrain-based method for the present work. A constant inherent strain was assumed, and application was done layer-by-layer. This approach has also been called the ' mechanical layer equivalent ' [24] and was used in this study. Mechanical layer equivalent approach (a numerical simulation approach) is based on the inherent strain concept and works on the macroscopic level. It is assumed that each microscopic layer (or micro-weld) in the SLM additive manufacturing undergoes similar thermo-mechanical conditions. This approach reduces the computational time and therefore can be applied to large parts.

The contour method is an experimental residual stress measurement technique. Fig. 1 shows the working principle of the contour method. In this method a sample of interest is cut into two halves with wire electrodischarge machining (WEDM). Owing to the residual stress in the sample the cut surface distorts. The stress component being measured is the normal to the cut surface. The relaxed surface pro fi le of both cut surfaces is measured with a coordinate measuring machine (CMM). The captured surface displacement data are then averaged, cleaned and smoothed. Then a three-dimensional fi nite-element (FE) model of one of the cut surfaces is built, and the reverse of the measured contour is applied to it as displacement boundary conditions. Finally a linearelastic FE analysis is performed to calculate the residual stress in the sample [25].

For the contour method the cutting operation is the fi rst and most in fl uential, as a number of errors can be incorporated into the fi nal results [26]. Wire EDM is the only method presently used for applying the contour method. Other cutting techniques (e.g. water jet cutting, laser cutting, etc.) may not work for the contour method owing to localized surface deformation, re-cutting the already cut surface, or greater surface roughness. Wire EDM machine low power settings tend to avoid a number of errors arising from surface roughness and changes in the material properties. Wire EDM cutting artefacts have an impact on the residual stress estimation, therefore where necessary a procedure for determination and correction of the cutting artefacts should be carried out [27].

In this paper the contour method was selected to estimate the residual stress along the SLM samples ' build direction as well as to validate the results of the numerical simulation. The contour method was applied to measure a single residual stress component along the build direction in titanium (Ti-6Al-4V) and Inconel 718 samples which were fabricated by the selective laser melting (SLM) additive manufacturing process. The titanium samples were of double cantilever geometry and had a distortion from the manufacturing process (Fig. 2a), whereas no signi fi cant visible distortion was seen for the Inconel cubes (Fig. 2c). One of the biggest advantages of the contour method is that it provides a full through-thickness and two-dimensional residual stress map. It is not sensitive to material microstructure as compared to di ff raction techniques such as X-ray di ff raction (XRD) and neutron di ff raction (ND). Also, the contour method is relatively easily accessible compared to neutron and synchrotron XRD sources, which only have a few installations around the world.

(a)

(b)

5

(c)

Cut location

L11 mm

Fig. 2. Additively manufactured samples (a) Titanium (Ti-6Al-4V) cantilever sample; (b) Dimensions of titanium (Ti-6Al-4V) cantilever sample (all dimensions are in mm), and (c) Inconel 718 sample.

<!-- image -->

Displacement (mm)

0.04

0.02-

0

-0.02

-0.04

-0.06 →

20

10

Y (mm)

## 2. Methodology

Two titanium (Ti-6Al-4V) and two Inconel 718 SLM additively manufactured samples were used in this study. Fig. 2 shows the samples used. The size of the Inconel cube was 20 × 20 × 20 mm 3 and the dimensions of the titanium double-cantilever sample are shown in Fig. 2(b). Note that in this case the titanium coupons were scaled up to double the usual size in order to make it easier to perform an accurate measurement. With the geometrical scale-up, however, the risk of cracking increases, and the present coupons indeed cracked near the attachment to the baseplate, at or very near the end of the printing. The cantilever-type samples have been used in powder-based additive manufacturing to study the distortion associated with the process [9], as they result in signi fi cant distortion which is easy to measure.

A number of titanium cantilever samples were built on machines from di ff erent vendors using their proprietary and optimized build parameters. The part-to-part variability in distortion was measured by making builds with multiple cantilevers spread throughout the build volume. The build-to-build variability in distortion was measured by including one such cantilever in seven di ff erent production builds. The distortion was found to be always within ± 5% of the average of the total population. This result will of course depend on the stability of the user-controlled build parameters. The residual stress measurements were done on only a few of the cantilevers, and were assumed to be fully representative of the entire population. The optimized SLM process parameters for the titanium cantilevers were then also used for the Inconel cubes.

The SLM printing parameters which were same for both titanium and Inconel samples are as follows:

- 30 μ m layer thickness
- Stripe scanning for in fi ll, stripe width 5 mm
- Three contour passes in each layer
- 67° layer-to-layer rotation

The laser power and speed were adjusted to achieve a stable process. No further changes to the process parameters were made during the build process. The main focus of the study was to predict and measure residual stress after the stable build and therefore the e ff ect of

0.02

0.01

Fig. 3. Isometric view of surface displacement pro fi le of titanium (Ti-6Al-4V) cantilever sample.

<!-- image -->

the individual process parameters was not considered. The additive layers build-up direction for the titanium cantilever sample is also shown in Fig. 2(a).

A number of cutting trials were carried out to select the wire EDM machining parameters before undertaking the contour method cutting of the titanium (Ti-6Al-4V) cantilever samples. For this purpose small cubes of 20 mm size were used, which were made with similar material and manufacturing process. The main aspects investigated for optimization in the cutting trials were the surface roughness and cut surface pro fi le. The samples were cut on a Fanuc Robocut α -C600i wire electric discharge machine with a 0.25-mm-diameter brass wire: a 0.1-mmdiameter brass wire was also trialed however it resulted in wire breakage during the cut. A small diameter wire removes less material and is therefore most suitable for thin parts. The samples were symmetrically clamped and water injection nozzles from top and bottom sides of the samples were used to fl ush the removed material. The contour cut location for the stress component of interest ( i.e. , along the build direction) of the titanium cantilever sample is shown in Fig. 2(a).

The surface displacement pro fi les of the cut halves of the samples were measured with a Zeiss Contura g2 coordinate measuring machine (CMM) by using a 3-mm-diameter touch probe. The distance between the measurement points as well as from the sample perimeter was set as 0.25 mm. The measurements were carried out in a temperature-controlled room. The displacement data from the cut surfaces of the samples were processed with Matlab data analysis routines for alignment, averaging, cleaning, fl attening and smoothing [28]. For data smoothing a cubic spline with a knot spacing of 4 mm was used. For fi nite element (FE) analysis the geometry of one cut half of the sample was modelled. An 8-node brick element in Abaqus software with a non-uniform mesh was used. The FE mesh converges to a distance of 0.1 mm between adjacent nodes at the sample edges, and in the center region of the samples this distance was about 0.5 mm. A linear-elastic FE analysis was performed. The following material properties were used:

Modulus of elasticity E =105GPa,Poisson ' s ratio ʋ =0.342

The minimum material mechanical properties for the SLM Ti-6Al-4V are experimentally determined and are as: Modulus of elasticity E =105GPa, Yield strength = 1020 MPa, Ultimate tensile strength = 1150 MPa

The contour cut location for the Inconel 718 sample is shown in

S, S33

(Avg: 75%)

(a)

S, S33

(Avg: 75%)

+9.210e+02

7

+8.163e+02

6

+ +-

.115e+02

068e+02

SóNŃ+++

. 3006+01

+01

+02

MNmM

(b)

-3

Fig. 4. Comparison of contour stress maps of titanium (Ti-6Al-4V) cantilever samples (a) No. 1, and (b) No. 2.

<!-- image -->

Fig. 5. Locations of highest tensile residual stress seen in titanium (Ti-6Al-4V) cantilever samples.

<!-- image -->

Stress (MPa)

Y

700

600 -

500 -

400

300

200 -

100

-100

-200

-300 -

-400

Note: Lines no. 1 &amp; 4 are along sample edges

(a)

Stress (MPa)

(b)

0

2

1000

800 -

- Line2-sample 1

-- Line2-sample 2

* Line3-sample 1

- Line3-sample 2

<!-- image -->

- Line5-sample 2

Fig. 6. Locations and directions of stress line pro fi les for both titanium (Ti-6Al4V) and Inconel 718 samples.

400 -

200 -

-200 -

-400

Fig. 7. Stress pro fi les for two titanium (Ti-6Al-4V) samples along (a) Lines 2 &amp; 3, and (b) Lines 5 &amp; 6.

<!-- image -->

<!-- image -->

Fig. 2(c). Both samples were cut with a 0.25-mm-diameter brass wire. The measurement setup and procedure for the Inconel samples was similar to the titanium cantilever samples. In this case for the fi nite

5

4

element (FE) analysis a uniform mesh on the cut surface was used with a distance of 0.2 mm between adjacent FE nodes. The following material properties were used:

Modulus of elasticity E =200GPa,Poisson ' s ratio ʋ =0.278

For numerical simulation the mechanical layer equivalent approach was used for both sample types (i.e. titanium Ti-6Al-4V &amp; Inconel 718), by adding layers of fi nite elements one by one with the *Model Change keyword in the commercial fi nite element solver Abaqus. Hexahedral meshes with linear reduced integration elements of 0.25 × 0.25 ×0.25mm 3 size were used. The nodes of the faces on the baseplate were completely constrained during the build simulation: U1 = U2 = U3=0. To simulate the cutting of the coupon from the baseplate, an analysis step was added in which these boundary conditions were changed to purely isostatic. The inherent strain was applied directly to the integration points of the elements being added, using Abaqus ' UEXPAN interface. All elements, either already added or being added in the current time step, were given the same elastic-plastic material properties.

## 3. Results

The surface displacement pro fi le (for the measured stress component) of the titanium (Ti-6Al-4V) cantilever sample is shown in Fig. 3. The data shown are the averaged data of the two cut halves and gives a su ffi ciently smooth relaxed surface pro fi le (Fig. 3). The contour stress maps for the two titanium cantilever samples are shown in Fig. 4. Tensile residual stress in the sample build-up direction (i.e. from one layer upward to the next) and at its mid height is seen along the edges of the samples. Comparative to other locations in the sample high tensile residual stresses are seen along line 1 (as per Fig. 6). The locations of the samples that gave highest tensile residual stress are shown in Fig. 5 and these locations are around the start and end locations of the line 1 (as per Fig. 6). The high tensile residual stresses along line 1 may pertain to SLM printing sequence (i.e. start of printing). The compressive residual stress mainly occupied the center region of the samples. A similar trend of the stress pro fi le was seen for both samples.

Sample no.1: Tensile residual stress = 905 MPa, Compressive residual stress = -335 MPa

Sample no.2: Tensile residual stress = 920 MPa, Compressive residual stress = -334 MPa.

Comparatively a slight variation in stress magnitude is also seen along the edges of these two samples.

Fig. 7 shows the comparison of the stress line pro fi les for the two titanium samples along lines 2, 3, 5 &amp; 6 (as per Fig. 6). The stress line pro fi les along the center and diagonal of the samples showed little variation in the stress distribution and magnitude. Nearly identical stress pro fi les for both samples shows excellent repeatability for the contour method results at these particular locations.

For a more detailed presentation of the stress distribution in the sample, a number of lines/locations are identi fi ed for the extraction of line plots as shown in Fig. 6.

The surface displacement pro fi le of the Inconel 718 sample is shown in Fig. 8. The displacement data plotted are the averaged data from the two cut halves of the sample.

The contour stress maps for the Inconel 718 samples no. 1 &amp; 2 are shown in Fig. 9. Tensile residual stress in the build-up direction for these samples was also seen along the edges of the samples. The residual stress distribution in the Inconel samples is similar to the titanium cantilever samples (as noted earlier). Compressive residual stresses were present at the center region of the samples. Both samples showed similar stress distribution with small variation in the stress magnitude.

0.02

Displacement (mm)

0.01

0

-0.01

-0.02

-0

.03

-0.04

20

- 0.015

Fig. 8. Isometric view of surface displacement pro fi le of Inconel 718 sample.

<!-- image -->

The samples no.1 &amp; 2 showed the following peak residual stress values:

Sample no.1: Tensile residual stress = 805 MPa, Compressive residual stress = -434 MPa

Sample no.2: Tensile residual stress = 837 MPa, Compressive residual stress = -459 MPa.

The slight variation between stress magnitudes in the Inconel samples particularly at the near surface locations, other than fl uctuations in the additive manufacturing process parameters, may pertain to errors arising from the wire EDM cutting, CMM measurement, and data smoothing [25].

The line pro fi les of residual stress for the Inconel samples are compared in Fig. 10. Fig. 10(a) gives the variation of stress along the center locations (i.e. along lines 2 &amp; 3 as per Fig. 6) of the samples, and Fig. 10(b) shows the stress line pro fi les along the diagonals (i.e. along lines 5 &amp; 6 as per Fig. 6) of the samples. Only a slight variation in the stress pro fi le along these lines can be seen.

Residual stresses predicted by the simulation for the titanium (Ti6Al-4V) cantilever coupon, and for the stress component of interest at the mid build height is shown in Fig. 11. The scale for Fig. 11 is adjusted with respect to the contour method stress results shown in Fig. 4. Tensile residual stresses were seen at and near the surface of the square block. Compressive residual stresses were present below and around the center of the square block surface. The square block corners showed lower tensile residual stress compared to the center region of the edges.

The residual stress prediction for the Inconel 718 is shown in Fig. 12. The Inconel 718 coupon showed tensile residual stresses at and near the outer surface, and compressive residual stresses below the outer surface and in the center of the coupon. Similar to the titanium sample, the Inconel coupon corners showed lower tensile residual stress in comparison to the center of the edges. However contrary to the titanium coupon the depth of the tensile residual stress at the opposite edges stays the same.

## 4. Discussion

The titanium (Ti-6Al-4V) cantilever samples used in this study showed signi fi cant distortion following fabrication. The contour method measurements were performed at the center of the square block region in the sample. The shape of residual stress distribution was found to be identical in each titanium (Ti-6Al-4V) and Inconel 718 sample, with little variation in stress magnitudes and depth of tensile residual stress, although there was di ff erence in the stresses between the two materials as a consequence of the di ff erent properties. The titanium and Inconel samples showed the following maximum residual stress values:

Titanium: Tensile residual stress = 920 MPa, Compressive residual stress = -335 MPa.

Inconel: Tensile residual stress = 837 MPa, Compressive residual stress = -459 MPa.

The contour method results showed highest magnitude of tensile residual stress at the corners of the samples.

The titanium coupon partially detached from the baseplate due to cracking. Fig. 13 shows the cracking that occurred at or very near the end of printing. The high temperature gradient and developed residual stresses can often lead to formation of cracks during SLM [29]. A similar simulation approach was used for both titanium and Inconel coupons. However for the titanium coupon additional simulation was done to account for the cracking, and this then showed a slightly di ff erent stress distribution for the titanium coupon as compared to the Inconel.

High tensile residual stresses approaching 875 MPa have been reported in bridge-shaped Ti-6Al-4V coupons manufactured with powderbed fusion additive manufacturing [30]. The residual stress associated with the SLM additive manufacturing of titanium (Ti-6Al-4V) has been previously found to be close to the material yield strength, and the stresses were seen to be higher in the direction of samples build-up [9].

In these coupons, the highest tensile residual stresses occurred at the surface. Agreement between predicted stress fi eld and measurements is acceptable given the low computational cost: a simulation based on the constant inherent strain takes little time to set up, is very robust with respect to convergence and can be completed in minutes, depending on the implementation and hardware available [20].

Line pro fi les of the residual stress obtained with numerical simulation and contour method for the titanium (Ti-6Al-4V) coupon are compared in Fig. 14. The line numbers are as per Fig. 6. The correlation between the experimental results from the contour method and the numerical simulation is quite good ( i.e. , with respect to stress pro fi le and magnitude) for the diagonal line no. 6. The stress pro fi le along line no. 3 also showed reasonably good correlation, however the near

S, S33

(Avg: 75%)

+6.210e+02

+5.130e+02

+4.050e+02

+2.970e+02

+1.890e+02

+8.100e+01

-2.700e+01

-1.350e+02

-2.430e+02

-3.510e+02

-4.590e+02

(a)

S, S33

(Avg: 75%)

+8.370e+02

+7.290e+02

+5.130e+02

+6.210e+02

+4.050e+02

+2.970e+02

+1.890e+02

-2.700e+01

+8.100e+01

-1.350e+02

-2.430e+02

-3.510e+02

-4.590e+02

(b)

Fig. 9. Comparison of contour stress maps of Inconel 718 samples (a) No. 1, and (b) No. 2.

<!-- image -->

surface tensile residual stress was not well-correlated. The contour method results showed highest magnitudes of the tensile residual stress at the corners, whereas numerical simulation predicted it at the center of the edges of the coupons. This situation is clearer from the stress along lines no. 1 &amp; 4. From the stress pro fi les for lines no. 2 &amp; 3 it was found that the two opposite edges of the titanium coupon showed greater depth of tensile residual stress, which is con fi rmed by both contour method and simulation.

Line pro fi les of residual stress for the Inconel 718 coupon are compared in Fig. 15. The stress pro fi les for lines no. 1 &amp; 4 again showed that the contour method measured highest tensile residual stress at the corners, while the numerical simulation predicted highest tensile residual stress at the center of the edges. The simulation results showed that the magnitude and depth of the residual stress at all four edges is identical, which slightly contradicts the contour method results. A satisfactory correlation was achieved below the surface of the coupons from both approaches.

The agreement between the residual stress measured with the contour method and predicted with the numerical simulation approach is satisfactory for the stress component of interest. Obtaining an accurate residual stress distribution near-surface with the contour method is challenging due to errors arising from WEDM, CMM and the data smoothing. During the WEDM cutting the surfaces of the sample at the locations of start &amp; end of cutting as well as at EDM wire entry &amp; exit locations are more prone to errors [26]. These errors arise due to different material removal rate at those locations. Sacri fi cial layers have

Stress (MPa)

(a)

Stress (MPa)

(b)

600

400

200

0

-200 -

-400 -

800 -

600 -

400 -

200

0

-200 -

-400

0

2

2

4

4

6

6

- Line2 - sample 1

—·- Line2 - sample 2

- Line3 - sample 1

-·- Line3 - sample 2

6

8

10

12

Distance (mm)

· - Line5 - sample 1

·- Line5 - sample 2

- Line6 - sample 1

- Line6 - sample 2

31

2

T

10

12 14 16 18 20 22

Distance (mm)

Fig. 10. Stress pro fi les for the Inconel 718 samples along (a) Lines 2 &amp; 3, and (b) Lines 5 &amp; 6.

<!-- image -->

been used in the past around the perimeter of the cut surface to minimize the magnitude of such errors [27]. Also the measurement of displacement pro fi le of the cut surface near the sample edges may not be accurate due to slippage of the measurement probe. A small diameter CMM probe might be useful to avoid slippage to some extent near the sample edges.

The overall agreement between the results from numerical simulation and the contour method measurements is interesting from an industrial point of view, given the low cost and low lead-time of the numerical simulation based on the inherent strain.

## 5. Conclusions

In this study residual stresses were characterized in SLM additively manufactured titanium (Ti-6Al-4V) and Inconel 718 coupons using a numerical simulation (inherent-strain-based method) and experimentally with the contour method. It was found that high tensile residual stress is present near the surface and along the edges of the samples. Compressive residual stress was seen at the center region of the samples. A good correlation was achieved between the numerical predictions and the contour method.

The key fi ndings are summarized as below:

- SLM additive manufacturing developed high magnitude of tensile residual stress along the build direction, at the outer surfaces of the titanium (Ti-6Al-4V) and Inconel 718 coupons. Compressive residual stress was present at the center region of both alloys.
- A good correlation of residual stress was achieved between the numerical simulation and the contour method. The correlation was particularly good below the surface (&gt; 1 mm depth) of the samples.
- The numerical simulation showed highest magnitude of tensile residual stress at the center of the edges for both types of samples. The contour method measurements showed highest tensile residual stresses at the corners of the both titanium and Inconel samples.
- Additional simulation was performed for the titanium coupon to account for the partial detachment of sample from the base plate due to cracking that occurred at near or end of printing the samples. This led to slight variation seen between the simulation results of the titanium and Inconel coupons.

S, S33

+1.092e+03

S, S33

(Avg: 75%)

+9.665e+02

(Avg: 75%)

+5.893e+02

+4.635e+02

+3.377e+02

+8.162e+02

+

+

.068e+02

7.115e+02

+2.120e+02

+8.620e+01

- 3.957e+01

5

- 1.653e+02

+

.020e+02

+

.972e+02

-4.169e+02

MN

-2.911e+02

1.878e+02

++

.925e+02

Numerical simulation

+

8

.300e+01

result

.175e+01

.312e+02

.265e+02

3

-1.014e+03

.360e+02

Numerical simulation result

5, 533

+8.370e+02

(Avg: 75%)

+7.290e+02

+6.2108+02

+5.130e+02

+4.0508+02

+2.970e+02

Fig. 11. Predicted residual stress in build-up direction of titanium (Ti-6Al-4V) cantilever, halfway through the build height and its comparison with contour method results (sample no. 2).

<!-- image -->

Fig. 12. Predicted residual stress in build-up direction of Inconel 718 cube, halfway through the build height and its comparison with contour method results (sample no. 2).

<!-- image -->

Stress (MPa)

Stress (MPa)

(a)

(a)

Stress (MPa)

Stress (MPa)

(b)

(b)

1200

1000

1000

800

600

600

Layers build-up direction

400

400

200

200

0

-200 -

-200

-400 -

-400

-600

1000

1200

1000

800

800 -

600

600 -

400 -

400 -

200

200

-200

-200

-400 ·

-400

0

2

4

2

4

ĐE //KH/HH/H//H//7

- Line 3 - Simulation

-·- Line 3 - Simulation

·

Line 3 - CM

- Line 3 - CM

Line 6 - Simulation

Line 6 - Simulation -

· Line 6 - CM

Line 6 - CM

<!-- image -->

IAAAAAAAAAAAA

Fig. 13. Partial detachment of the titanium (Ti-6Al-4V) samples from the base plate.

-O- Line 1 - Simulation

· - Line 1 - CM

-O- Line 1 - Simulation

·- Line 1 - CM

Line 2 - Simulation

- Line 2 - CM

-·- Line 2 - Simulation

A - Line 4 - Simulation

- Line 2 - CM

- Line 4 - CM

- Line 4 - Simulation

A - Line 4 - CM

4

6

4

Distance (mm)

Distance (mm)

Fig. 14. Comparison of simulation and contour method stress pro fi les for the titanium (Ti-6Al-4V) samples along (a) Lines 3 &amp; 6, and (b) Lines 1, 2 &amp; 4, for the lines de fi ned in Fig. 6.

8

8

0

0

2

2

10

10

Fig. 15. Comparison of simulation and contour method stress pro fi les for the Inconel 718 samples along (a) Lines 3 &amp; 6, and (b) Lines 1, 2 &amp; 4, for the lines de fi ned in Fig. 6.

## Acknowledgements

We are grateful to Andreas Nick from the Airbus APWorks Germany, for facilitating the project and providing the samples. Further thanks to Steve Damms at The Institute for Advanced Manufacturing and Engineering for his help with the WEDM. M. E. Fitzpatrick is grateful for funding from the Lloyd ' s Register Foundation, a charitable foundation helping to protect life and property by supporting engineeringrelated education, public engagement and the application of research.

## References

- [1] B. Dutta, F.H. Froeas, The additive manufacturing (AM) of titanium alloys, Met. Powder Rep. 72 (2017) 96 -106.
- [2] I. Gibson, D. Rosen, B. Stucker, Additive Manufacturing Technologies, 3D Printing, Rapid Prototyping And Direct Digital Manufacturing, Springer Science + Business Media, New York, 2015.
- [3] P.K. Gokuldoss, S. Kolla, J. Eckert, Additive manufacturing processes: selective laser melting, electron beam melting and binder jetting -selection guidelines, Materials 10 (2017) 672.
- [4] P. Mercelis, J.-P. Kruth, Residual stresses in selective laser sintering and selective laser melting, Rapid Proto. J. 12 (2006) 254 -265.
- [5] Y. Liu, Y. Yang, D. Wang, A study on the residual stress during selective laser melting (SLM) of metallic powder, Int. J. Adv. Manuf. Technol. 87 (2016) 647 -656.
- [6] N. Kalentics, E. Boillat, P. Peyre, C. Gorny, C. Kenel, C. Leinenbach, J. Jhabvala, R.E. Loge, 3D laser shock peening -a new method for the 3D control of residual stresses in selective laser melting, Mater. Des. 130 (2017) 350 -356.
- [7] C. Li, J.F. Liu, Y.B. Guo, Prediction of residual stress and part distortion in selective laser melting, Procedia CIRP 45 (2016) 171 -174.
- [8] P.K. Gokuldoss, S. Kolla, J. Eckert, Additive manufacturing processes: selective laser melting, electron beam melting and binder jetting - selection guidelines, Materials 10 (2007) 672.
- [9] B. Vrancken, V. Cain, R. Knutsen, J.V. Humbeeck, Residual stress via the contour method in compact tension specimens produced via selective laser melting, Scripta Mater. 87 (2014) 29 -32.
- [10] C. Li, J.F. Liu, X.Y. Fang, Y.B. Guo, E ffi cient predictive model of part distortion and residual stress in selective laser melting, Addit. Manuf. 17 (2017) 157 -168.
- [11] N.E. Hodge, R.M. Ferencz, R.M. Vignes, Experimental comparison of residual stresses for a thermomechanical model for the simulation of selective laser melting, Addit. Manuf. 12B (2016) 159 -168.
- [12] R.J. Moat, A.J. Pinkerton, L. Li, P.J. Withers, M. Preuss, Residual stresses in laser direct metal deposited waspaloy, Mater. Sci. Eng. A 528 (2011) 2288 -2298.
- [13] T. Simson, A. Emmel, A. Dwars, J. Bohm, Residual stress measurements on AISI 316L samples manufactured by selective laser melting, Addit. Manuf. 17 (2017) 183 -189.
- [14] J.L. Bartlett, B.P. Croom, J. Burdick, D. Henkel, X. Li, Revealing mechanisms of residual stress development in additive manufacturing via digital image correlation, Addit. Manuf. 22 (2018) 1 -12.
- [15] J. Wu, L. Wang, X. An, Numerical analysis of residual stress evolution of AlSi10Mg manufactured by selective laser melting, Opt -Int. J. Light Electron. Opt. 30 (2017) 65 -78.
- [16] M. Shiomi, K. Osakada, K. Nakamura, T. Yamashita, F. Abe, Residual stress within metallic model made by selective laser melting, CIRP Ann. 53 (2004) 195 -198.
- [17] E. Denlinger, Thermo-Mechanical Model Development and Experimental Validation of Metallic Parts in Additive Manufacturing, PhD Dissertation, The Pennsylvania State University, 2015.
- [18] T. Fujimoto, A method for analysis of welding residual stresses and deformations based on the inherent strain method, J. Jpn. Weld. Soc. 39 (1970) 236 -252.
- [19] Y. Ueda, K. Fukuda, K. Nakacho, S. Endo, A new measuring method of residual stresses with the aid of fi nite element method and reliability of estimated values, Trans. JWRI. 4 (1975) 123 -131.
- [20] Y. Ueda, M.G. Yuan, A predicting method of welding residual using source of residual stress (report III), Trans. JWRI. 22 (1993) 157 -168.
- [21] M.P. Fransen, Eigenstrain Reconstruction of Residual Stresses Induced by Selective Laser Melting, MSc Dissertation, Delft University of Technology, 2016.
- [22] T. Mura, General theory of eigenstrains in: micromechanics of defects in solids, Mech. Elast. Inelast. Solids 3 (1987) 1 -73.
- [23] T.-S. Jun, A.M. Korsunsky, Evaluation of residual stresses and strains using the eigenstrain reconstruction method, Int. J. Solids Struct. 47 (2010) 1678 -1686.
- [24] N. Keller, V. Ploshikhin, New method for fast predictions of residual stress and distortion of AM parts, Annu. Int. Solid Freeform Fab. Symp. (2014) 1229 -1237.
- [25] M.B. Prime, Cross-sectional mapping of residual stresses by measuring the surface contour after a cut, J. Eng. Mater. Technol. 123 (2000) 162 -168.
- [26] F. Hosseinzadeh, J. Kowal, P.J. Bouchard, Towards good practice guidelines for the contour method of residual stress measurement, J. Eng. 2014 (8) (2014) 453 -468 http://digital-library.theiet.org/content/journals/10.1049/joe.2014.0134.
- [27] B. Ahmad, M.E. Fitzpatrick, Minimization and mitigation of wire EDM cutting errors in the application of the contour method of residual stress measurement, Metall. Mater. Trans. A 47 (2015) 301 -313.
- [28] G. Johnson, Residual Stress Measurement Using Contour Method, PhD Thesis The University of Manchester, 2008.
- [29] B. Zhang, Y. Li, Q. Bai, Defect formation mechanism in selective laser melting: a review, Chin. J. Mech. Eng. 30 (2017) 515 -527.
- [30] T. Mishurova, S. Cabeza, K. Artzt, J. Haubrich, M. Klaus, C. Genzel, G. Requena, G. Bruno, An assessment of subsurface residual stress analysis in SLM Ti-6Al-4V, Materials 10 (2017) 348.