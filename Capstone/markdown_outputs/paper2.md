<!-- image -->

Contents lists available at ScienceDirect

## Journal of Manufacturing Processes

journal homepage: www.elsevier.com/locate/manpro

## Multi-objective accelerated process optimization of mechanical properties in laser-based additive manufacturing: Case study on Selective Laser Melting (SLM) Ti-6Al-4V

Amir M. Aboutaleb a , Mohammad J. Mahtabi b , Mark A. Tschopp c,1 , Linkan Bian a, ⁎

- a Department of Industrial and Systems Engineering, Mississippi State University, MS, USA
- b Department of Mechanical Engineering, University of Tennessee at Chattanooga, Chattanooga, TN 37403, USA
- c U.S. Army Research Laboratory, Chicago, IL, USA

## A R T I C L E I N F O

Keywords: Laser-based additive manufacturing Tensile properties Design of experiments Multi-objective optimization Selective laser melting (SLM)

Ti-6Al-4V

## 1. Introduction

## 1.1. Objective and hypothesis

The objective of the present work is to apply a novel framework for efficiently optimizing multiple mechanical properties of metal parts fabricated by Laser-Based Additive Manufacturing (LBAM) systems. Inferior mechanical properties of parts fabricated by LBAM hamper the widespread adoption of this technology and accordingly achieving its full potential for fabricating functional parts in different industries. It is traditionally believed that improving the relative density of LBAMfabricated parts will result in superior mechanical properties. However,

⁎ Corresponding author.

E-mail address: bian@ise.msstate.edu (L. Bian).

1 ASME Fellow.

## A B S T R A C T

Process optimization of Laser-Based Additive Manufacturing (LBAM) systems is often complicated by the tradeoff between different mechanical properties as well as the relative density window. For instance, parts with similar relative densities can have noticeably different tensile mechanical properties (e.g., elongation-to-failure, yield strength, ultimate tensile strength, Young's modulus). This phenomenon can be attributed to the variation of size and distribution of fabrication-induced voids within the final parts. To overcome the aforementioned challenge, we applied an efficient sequential multi-objective process optimization framework to optimize the quality of LBAM-fabricated parts with respect to multiple non-correlated mechanical properties within the optimal relative density regime. The applied Multi-objective Accelerated Process Optimization (m-APO) method indirectly accounts for the effect of size and distribution of voids on the final parts' mechanical properties. The m-APO decomposes the master multi-objective optimization problem into a sequence of single-objective subproblems constructed from mathematically convex combination of individual unknown objective functions. At each step, the m-APO smartly maps the experimental data from previous sub-problems to the remaining subproblems. Therefore, the information captured from previous sub-problems is leveraged to accelerate the master multi-objective process optimization problem. The m-APO exhibited capability to achieve a set of process parameter setups, resulting in the best trade-off between conflicting mechanical properties in the optimal window. The m-APO methodology is employed to maximize relative density and elongation-to-failure of Ti-6Al4 V parts fabricated by Selective Laser Melting (SLM) system. The results show that the m-APO achieved the optimal process parameter setups while reducing the time-and cost-intensive experiments by 51.8%, compared with an extended full factorial design of experiments plan.

our initial experimental study reveals that obtaining a high relative density for the LBAM-fabricated parts (compared to the traditional counterpart) does not necessarily result in acceptable tensile mechanical properties, such as elongation-to-failure. This phenomenon can be attributed to the existence of different size and distribution of fabrication-induced voids in the final part. The goal of the present work is to employ an efficient multi-objective process optimization framework to optimize quality of LBAM parts with respect to multiple properties such as relative density and elongation-to-failure. The central hypothesis is that breaking down the master multi-objective problem into an intelligently-defined sequence of scalar combination of objective functions, as a set of sub-problems, can optimize conflicting mechanical

<!-- image -->

<!-- image -->

(a)

(b)

(c)

(d)

(e)

Fig. 1. Schematic indicating the various possible distribution of voids for samples with similar densities, which may result in different tensile properties.

<!-- image -->

properties with the fewest experimental runs. The hypothesis is tested against experimental data on Ti-6Al-4V parts fabricated by Selective Laser Melting (SLM) system. This work leads to a generic multi-objective process optimization framework that can be applied to any LBAM system, with any material, for optimizing any scalar mechanical property.

## 1.2. Motivation

Titanium alloys, among them Ti-6Al-4V, show superior mechanical properties such as high strength, high strength-to-weight ratio, high toughness, ductility, biocompatibility, and high resistance to severe environments. Due to these superior properties these alloys have been employed for several applications in various industries. For instance, titanium alloys, such as Ti-6Al-4 V, have been used in biomedical applications since they fulfill the requirements, namely high specific strength, good corrosion and fatigue resistance [1-4]. Moreover, opencell structures of highly porous metals are recognized very advantageous in orthopedic implants, due to the low modulus of elasticity (adjustable to that of bone) and high volumetric porosity (i.e. low relative density) [5,6]. In the dental prostheses applications, Ti-Ag and TiCu alloys are used-owing to their relatively high strength-in fabricating partial dentures, clasps and bridges [7,8]. Furthermore, titanium alloys are vastly employed in the aerospace industry because of the desired weight-saving property resulted from their high strength-toweight ratio [9-11]. In addition, in the automotive industry, where light-weight materials with an acceptable relative density and strength are required, titanium alloys are favorable candidate materials [12,13].

Fabrication of Ti-6Al-4V coupons and parts using Laser-Based Additive Manufacturing (LBAM) techniques has rapidly grown in the past decade, due to their popularity for different applications. One of the main challenges of manufacturing AM metallic alloys is to obtain similar, or even higher, mechanical properties than the conventional alloy. To achieve this, a set of appropriate process parameters, such as laser power, scanning speed, hatch spacing, etc., should be employed during LBAM [14,15]. Therefore, the problem of optimizing process parameters to obtain acceptable mechanical properties, compared to the traditional counterparts, has been addressed by several researchers [14-17].

Due to nature of fabrication in LBAM, the manufactured parts are highly prone to formation of microstructural defects, such as voids and pores, which results in lower relative density of the material, as well as significantly reduced mechanical strength [16,18]. For LBAM applications, it is generally believed that maximizing the part density results in the optimal level of mechanical properties (such as elongation-tofailure), which is typically true. Hence, a data-driven methodology using Bayesian theorem was developed to optimize a single mechanical property-such as part's relative density-called Accelerated Process Optimization (APO) [15]. The APO technique resulted in an average relative density of 99.2% for stainless steel parts fabricated by Selective Laser Melting (SLM) after only five experiments [15]. Nevertheless, further experimental studies revealed that maximizing the relative density of the part, although necessary, might not be sufficient to achieve acceptable mechanical properties. We demonstrate the insufficiency of considering high relative density of the LBAM product as the only optimization objective by a few examples. For instance, fatigue resistance of specimens fabricated using LBAM techniques, even with very high relative densities, have been reported to be much lower than that for specimens from conventional methods [19,20]. This lower fatigue behavior was attributed to the planar, low-volume voids in the parts that do not affect the density but significantly influence the fatigue resistance [19].

Several factors can potentially cause lower mechanical properties, while having improved relative density, and high cooling rate associated with LBAM is one of them [16,18]. For instance in SLM, high cooling rate can cause low ductility in the final part for metallic powders [21]. Although the high cooling rate during most LBAM processes results in high yield strength, it causes low elongation-to-failure [22].

The shape and distribution of the pores is another significant factor causing the aforementioned conflicting behavior amongst different mechanical properties [19]. For instance, different parts with almost the same relative density can have different pore distribution. This phenomenon is schematically illustrated by Fig. 1. In Fig. 1, each gray dot represents a void with the same shape and volume. Although all the five parts have hypothetically same relative density (because of similar number of voids), distribution of the voids changes from one to another. For instance, the part (a) has a very congested distribution of voids at the middle of the gauge section of the part; while the voids are distributed close to the grip ends in part (b). Moreover, in parts (c) and (b) voids are formed very close to the surface of the specimen at the gauge section with different patterns, while those are almost evenly distributed inside the specimens shown in part (e). Other than the pore distribution, pores' shape can significantly contribute to the final parts' mechanical characteristics, such as tensile properties. In practice, the pores can have very different shapes and volumes. Fig. 1(e) represents some microscopic longitudinal pictures of pores within one part. The intent of the presented work is to apply an efficient data-driven experimental plan to achieve the best tradeoff amongst different

1400

(a)

0.0550

1000

0.0500

800

600

0.0475

400

0.0450

200

0

0.145

0

&lt; 0.0

- 0.2

-

<!-- image -->

0.150

0.01

Fig. 2. (a) Contour plot of part density versus hatch spacing and layer thickness. (b) Contour plot of part elongation-to-failure ( f) versus hatch spacing and layer thickness (laser power is set to 400 w and response values are scaled within [FRO] range).

properties of the final parts, which could indirectly consider the effects of void size and distribution.

Fig. 2 illustrates the contour plots of relative density and elongationto-failure versus hatch spacing and layer thickness for Ti-6Al-4 V parts fabricated by SLM in our initial experimental studies (see Section 3.1.2 for details). From Fig. 2, it is evident that both relative density and elongation-to-failure for parts made by varying hatch spacing and layer thickness cannot be maximized simultaneously. The combinations of process parameters around the area in the middle right of Fig. 2 (a) result in maximum relative density. However, the same process parameter setup results in low elongation-to-failure (area in the middle right of Fig. 2 (b)). Considering such a coupled variation amongst various mechanical properties, it is extremely challenging to identify the optimal process parameter setup that results in parts with acceptable mechanical properties. Therefore, this work addresses the following challenging research question in LBAM: What experimental plan is required to optimize process parameter setup with respect to multiple mechanical properties of part?

## 1.3. Research challenges and overview of the proposed approach

As discussed before and shown on Fig. 3, tensile mechanical response of the AM Ti-6Al-4 V is highly sensitive to the selected process parameters, including laser power, scanning speed, hatch spacing and layer thickness. This sensitivity is mainly due to differences in size, shape, location and distribution of fabrication-induced vides, pores, and un-melted regions due to lack of fusion. Consequently, an undesirable amount and distribution of voids can result in very low elongation-tofailure as well as a low failure stress. On the other hand, a low void volume fraction and un-melted regions that are distributed uniformly can enable a large elongation-to-failure and a high failure stress.

Traditionally, maximizing the relative density of the LBAM material was considered as the objective to find the optimized process parameters in a LBAM system [15]. However, for the same relative density, size, shape and distribution of the voids can also dominate the mechanical properties of the LBAM material. Therefore, an extra criterion needs to be considered in optimizing the process parameters to obtain superior mechanical properties. The selected additional criterion in optimizing the process parameters, should be an appropriate representative of the material response. While several mechanical properties-such as modulus of elasticity, ultimate stress, etc.-can be selected, when dealing with one material (as the case of Ti-6Al-4 V in this study), elongation-to-failure can be an appropriate candidate for the additional optimization objective. Employing elongation-to-failure ( ε f ) is also governed by the stress-strain response of the material, where beyond yield point, a wide range of ε f can be associated with an almost constant stress (see the flat region on the longest stress-strain curve on Fig. 3). Thus, use of the ultimate stress may not be reasonable since knowing this parameter may not provide enough information about the elongation-to-failure. On the other hand, not only ε f implicitly accounts

Fig. 3. Selected stress-strain curves of the different specimens fabricated with different process parameters, indicating the sensitivity of the tensile properties to the process parameters.

<!-- image -->

0.3

Layer Thickness (mm)

Density

&lt; 0.080

0.080 - 0.162

0.162 - 0.244

0.244 - 0.326

(b)

Layer Thickness (mm)

0.0550

0.0525-

0.1

0.2

1.0-

0.8 -

0.6-

0.4-

0.2-

0.0-

·

0.0

·

<!-- image -->

0.2

Fig. 4. The representation of the data scatter plot to illustrate correlation between scaled part relative density and scaled elongation-to-failure (data are scaled within [FRO] range). Relative density and elongation-to-failure are positively correlated in general (see the left plot). However, they are negatively correlated in the optimal window corresponding to the relative density (see the right plot).

for the value of the material's ultimate stress, it can also demonstrate the toughness of the material. As a result, elongation-to-failure of the material was selected as the additional constraint for the optimization of process parameters in this study.

Although the conventional belief regarding the existence of positive correlation between relative density and part's mechanical properties is correct in general, it may not necessarily hold in the optimal window corresponding to part relative density. This contradictory phenomenon is depicted by Fig. 4. The plot on the right illustrates the data scatter plot of the scaled relative density and the scaled elongation-to-failure for Ti-6Al-4 V parts fabricated by SLM (see Section 3.1.2 for details). The slope of line represents the Pearson correlation coefficient ( ) between relative density and elongation-to-failure. Although not very significantly, they are positively correlated ( % C80w8 ). However, if we look at the optimal window with respect to relative density (i.e., parts with scaled relative density greater than 0.82) we observe a converse phenomenon (The optimal relative density window can be any acceptable relative density depending on the application). The plot on the left illustrates the data scatter plot of the scaled relative density and the scaled elongation-to-failure for parts fabricated within optimal window. It is evident that relative density and elongation-to-failure are negatively correlated ( % C8DjD ). In other words, under the relative density optimal regime, there is no guarantee that improving the part density give rise to higher elongation-to-failure. With this in mind, our problem falls into the scope of multi-objective optimization. However, the existing multi-objective optimization methodologies are not wellsuited for optimizing LBAM processes with respect to multiple mechanical properties.

The existing multi-objective optimization methodologies fall into two major categories: (i) scalarization methods and (ii) evolutionary algorithms [23,24]. Scalarization methods, which are considered as the classical approach in the literature, aggregate multiple objective functions to reduce the multi-objective problem into a scalar or single-objective optimization problem, enabling the employment of single-objective optimization techniques [24,25]. This category of methodologies is not applicable for the current multi-objective mechanical properties optimization problem in LBAM because the functional form of the objective functions-representing the relationship between process parameters (e.g., hatch spacing and layer thickness) and quantities of interest (e.g., part density and elongation-to-failure)are unknown. Moreover, constructing the surrogate models representing the mathematical form of objective functions requires a large number of very time-and-cost intensive experimental data, which is not economically feasible for LBAM processes. In contrast to the classical scalarization methods, evolutionary algorithms directly generate a set of Pareto optimal solutions-representing permissible tradeoff between contradictory objective responses-in an iterative manner and gradually improve the quality of the Pareto optimal solutions [24,26-29]. This family of algorithms requires numerous objective function evaluations (i.e., many LBAM experimental runs in the current mechanical properties optimization problem). Hence, we do not apply them to address the current multi-objective process optimization problem since they result in an extremely high experimental cost. There is a serious research gap for optimizing multiple mechanical properties of LBAM fabricated parts in an efficient manner. In the present study, we apply a novel multi-objective process optimization framework to intelligently accelerate the process optimization and achieve a set of process parameters resulting in the best compromises between mechanical properties in the optimum regime.

The remainder of this paper is organized as follows. In Section 2, we review the existing literature concerning mechanical properties of parts fabricated by LBAM. In Section 3, we elaborate on the applied multiobjective process optimization approach. In Section 3.1.2, the proposed methodology is applied to a real-world case study to optimize mechanical properties of Ti-6Al-4 V parts fabricated by SLM. Finally, in Section 5, concluding remarks are provided.

## 2. Background: mechanical properties of laser-based additive manufacturing

Shamsaei et al. [22] conducted a literature review about recent advancements in Direct Laser Melting (DLD) systems and asserted that, due to the high cooling rate in DLD, (ultimate) tensile and yield strength of DLD parts are generally as good as those of wrought materials. Nevertheless, for most cases, elongation-to-failure of the DLD parts is lower than that for wrought materials. Non-optimized DLD process along with the associated micro-porosity and oxide inclusions in the parts are found to be the major cause of this phenomenon. Building orientation is another key factor affecting the part's tensile properties. In most cases, building the parts parallel to the loading direction, in tensile specimens, results in lower tensile strength compared to perpendicularly built specimens [22,30]. Different cooling rates resulted from different building orientation may be the reason for the aforementioned anisotropic behavior [22,30].

Selcuk et al. [31] reviewed and compared mechanical properties of parts fabricated by different LBAM systems. They divided LBAM systems into two major categories: (i) blown powder deposition and (ii) powder-bed deposition. Selcuk et al. [31] mentioned that mechanical properties of blown powder deposition systems (e.g., Laser Engineered Net Shaping-LENS) are fairly comparable to conventional manufacturing techniques. For instance, yield strength for stainless steel fabricated by LENS system is reported to be almost two times higher than that of conventionally processed material, while the ductility was halved. This different mechanical property between the LENS and

0.8 Г

0.74

0.61

·

wrought stainless steel was attributed to the resulted grain refinement in LENS-fabricated specimens. Almost the same case is reported for titanium- and nickel-based superalloys [31]. As it is mentioned by other papers, build direction is a key parameter affecting tensile properties of part [30-33]. For instance, yield strength of the stainless steel parts in the perpendicular direction to the build orientation is reported to be considerably lower than the parallel direction, while the opposite is reported for elongation-to-failure [31,32]. Even though anisotropic tensile behavior is a common characteristic of parts fabricated by both powder-bed deposition and blown powder deposition systems, its magnitude varies from material to material. For instance, this phenomenon is considerably greater for stainless steel compared to nickelbased superalloys [31]. Regarding anisotropy tensile behavior in powder-bed deposition systems, Selcuk et al. [31] reported the lowest strength and ductility for the specimens fabricated in vertical direction (applied load was perpendicular to the laser traverse direction). On the other hand, highest strength was observed for the horizontal direction, where the applied load was along the laser traverse direction. Similar to blown powder deposition system, elongation-to-failure for stainless steel parts fabricated by powder-bed deposition system in all directions is reported to be lower than those achieved by conventionally fabricated parts [31].

Carroll et al. [34] studied the effect of build orientation on tensile properties of Ti-6Al-4V parts fabricated by a directed energy deposition (DED) system. Results from their work show that without any postfabrication treatment and just by modifying the process parameters a larger elongation-to-failure can be achieved for DED Ti-6Al-4V alloys. The modified process parameters in Carroll et al. [34], were adjusted to reduce the amount of lack-of-fusion defects in the fabricated parts. Doing so, the achieved elongations-to-failure were reported to be 11% and 14% for the longitudinal and traverse directions, respectively, which showed significant improvement, compared to previous LBAM Ti-6Al-4V parts. Based on the literature, there has been a lot of research on build orientation effects on tensile properties of the LBAM material [34,35]. However, to the best of our knowledge, there is no research work on optimizing process parameters to achieve acceptable tensile properties and a high relative density of the AM material.

Wang et al. [36] studied the nucleation and propagation of fatigue cracks in TC18 titanium alloy fabricated by laser melting deposition (LMD) system. They reported that size and location of the fabricationinduced micropores and voids to be the main defects dominating the high-cycle fatigue (HCF) lives of this alloy. As expected, they reported less effect on HCF lives for smaller pores compared with larger ones. Moreover, the effect of pores located closer to the surface of the specimen were reported to be more detrimental on the HCF behavior of this alloy. Yadollahi et al. [37] also employed the crack-growth concept and investigated the effects of defect properties on the fatigue behavior of Inconel 718 alloy, fabricated by L-PBF method. Their study also indicated the defect (i.e. void) size to be the most influential defect feature on the fatigue life of AM Inconel 718. Therefore, employing a set of process parameters that result in no or very small voids in the fabricated parts is desired for durable LBAM materials.

There are some works related to advanced welding systems tried to predict and optimize the ultimate tensile strength of joints using conventional design of experiments (DOE) methods. Although welding processes may not fall into the category of LBAM processes; due to the layered nature of welding processes, results from such a study can potentially help to understand the appropriate criteria for optimizing the process parameter of AM process for favorable tensile behavior. Silva et al. [38] applied Taguchi orthogonal arrays to optimize ultimate tensile strength of aluminum alloy joints. Two different orthogonal arrays (i.e., ? 8V0 S R and ? 0RVO S wO ) were applied considering three different joint configurations (i.e., butt, T and double-pass overlap joints). Bozkurt [39] used ? 0RVO S wO Taguchi orthogonal arrays to maximize tensile strength of polyethylene sheets processed by friction stir welding process. Ampaiboon et al. [40] applied fractional factorial (x ' x ) design with two replication to optimize ultimate tensile strength of mild steel (ST37-2) joints welded by Metal Active Gas system. Same DOE procedures can be applied to optimize tensile strength of AM parts; however, they result in many expensive LBAM experimental trials. Furthermore, they cannot directly handle optimizing multiple uncorrelated properties. Therefore, a novel multi-objective DOE is employed in this study, which requires significantly less number of experiments and specimen fabrication using LBAM.

## 3. Methodology

## 3.1. Multi-objective process optimization

This section is dedicated to presenting an overview of the MultiObjective Accelerated Process Optimization (m-APO) methodology applied in the present work. The m-APO is a generalization of an existing Accelerated Process Optimization (APO) method, which is able to facilitate the optimization of AM systems with respect to one objective (e.g., one mechanical property of parts such as relative density) by characterizing and leveraging the similarities amongst the current and non-identical prior studies [15]. The APO is able to significantly reduce the number of experimental runs while achieving a targeted optimum value. In the authors' previous research work, the APO is applied to maximize the relative density of stainless steel test coupons fabricated by SLM system [15].

The m-APO applied in the present work is primarily developed to minimize the geometric inaccuracy of the AM parts [41-43]. In principal, the m-APO is developed and illustrated in the form of bi-objective process optimization; however, it can readily be extended to multiobjective cases. In the present study, we apply m-APO to maximize relative density and elongation-to-failure of Ti-6Al-4 V tensile samples fabricated by SLM system.

## 3.1.1. Multi-objective process optimization and pareto front

Assume that the goal is to maximize two response variables Y w and Y 0 which are not significantly positively correlated (e.g. part relative density and elongation-to-failure). The bi-objective maximization problem is demonstrated as follows:

<!-- formula-not-decoded -->

s

s

K

t

2

2

Y s V S denotes the vector of objective functions s s Y Y w w :j w :: P ) , and s is the vector of process parameters (e.g., layer thickness, laser power and hatch spacing). K denotes the design space consisted of all possible combinations of process parameters' values, i.e., s. Moreover, = C s s s S Y Y {( ( ), ( )) : } 1 2 2 denotes the objective space, i.e., the set of all possible combinations of response vectors Y corresponding to the design space.

Due to the very complex underlying thermo-mechanical process associated with melt-pool formation and solidification in LBAM, for most cases, the mathematical expression of s Y Pw : and s Y ) w : representing the functional relationship between the process parameters (i.e., s) and the mechanical properties of parts (i.e., Y w and Y 0 ) is not well-identified and formulated as yet. In other words, the analytical formula corresponding to the objective functions are unknown. Furthermore, statistical speaking, the correlation between s Y Pw : and s Y ) w : is also unknown a priori . Improving the value of s Y Pw : may consequently lead to worsening the value of s Y ) w : or vice versa. In practice, due to the potential low or even negative correlation between Y w and Y 0 , it may not be possible to optimize them using the same process parameter setup. For instance, in the presented optimal window-shown in Figure 4-there is a negative Pearson correlation between part relative density and elongation-to-failure, i.e., % C8DjD . Therefore, improving the part relative density will not guarantee improving the elongation-to-failure of parts. With this in mind, there is no unique set of process parameters

Max Z3 (s) = (0.7Y1 (s) + 0.3Y2(s))

S

S: Design space

C: Objective space as the optimal solution to the presented bi-objective process optimization problem. The ultimate goal of applying the m-APO-a novel methodical and optimization-oriented DOE procedure-in the present study is to efficiently achieve a set of optimal process parameter setups resulting in the best tradeoff between such contradictory mechanical properties in the parts.

Inspired by the scalarization idea, the m-APO convert the master biobjective process optimization problem into a series of single objective optimization sub-problems via multiplying each objective function by a weight coefficient. Therefore, the decomposed bi-objective maximization problem can be formulated as follows:

<!-- formula-not-decoded -->

<!-- formula-not-decoded -->

k h denotes weight coefficient corresponding to the k th objective function within the h th sub-problem. Different combinations of weight coefficients, satisfying the constant B % P h h P ) , corresponds to different sub-problems and accordingly different search directions on the objective space.

For instance, weight coefficients % (2ffi P x and % (2x ) x correspond to a sub-problem with the objective function in the form of = + s s s Max Z Y Y ( ) (0.7 ( ) 0.3 ( )) 3 1 2 . The weight coefficients ( k h ) represented by the tangent of the maximization objective function line in Fig. 5 denotes the desired search direction for the ff rd sub-problem. Another combination of weight coefficients, such as % (2x P fi and % (2ffi ) fi , corresponds to a distinct sub-problem with different objective function and search direction, i.e., = + s s s Max Z Y Y ( ) (0.3 ( ) 0.7 ( )) 4 1 2 in Fig. 5.

Likewise, different combinations of weight coefficients lead to entirely distinct shapes of contour plot for the weighted summation of part relative density and elongation-to-failure generated by our initial experimental data. For instance, Fig. 6 illustrates two contour plots corresponding to different combinations of weight coefficients for our initial experimental data; i.e., % % w Pj (: P P ) P and % % w (2xj (2ffi: P fi ) fi . It is visually noticeable that there is not a unique combination of hatch spacing and layer thickness maximizing both contour plots' response values. This statement is more supported by the research challenges regarding the negative or weak positive correlation amongst various mechanical properties of LBAM parts discussed in Sec.1.3. With this in mind, we also conclude that it is not possible to optimize infinite number of sub-problems by a unique set of process parameters. Therefore, in such problems, the optimum solution is a subset of objective space 7 representing the best compromises amongst the values of conflicting objective responses, i.e., Y P and Y ) .

The m-APO methodology is developed to systematically and efficiently identify the Pareto optimal solutions associated with the multiobjective optimization problem. A Pareto optimal solution s s Y Y V V S) V SS 1 1 w 0 is a non-dominated solution on the objective space representing one of the best feasible compromises amongst the objective functions' values. A design point s K 1 corresponding to a Pareto optimal solution is called an optimal design point if and only if there is no other s K such that s s Y Y V S V S 1 k k for % k w) 0 . With respect to our mechanical properties optimization problem, a Pareto optimal solution corresponds to a design point where there is no other one resulting in higher value of both part relative density and elongation-to-failure. The set of Pareto optimal solutions is called Pareto front. The concept of design space, objective space, Pareto optimal solution and Pareto front are illustrated by Fig. 5 given two process parameters for the bi-objective optimization problem presented by Eq. (2).

## 3.1.2. An overview of multi-objective accelerated process optimization (mAPO)

The Multi-Objective Accelerated Process Optimization (m-APO) methodology is targeted at achieving a well-distributed set of Pareto optimal solutions to efficiently approximate the Pareto front with very limited number of experiments. As opposed to conventional scalarization-based optimization approaches which individually solve the singleobjective sub-problems, the m-APO identifies and leverages the similarities amongst different sub-problems to eventually accelerate the multi-objective optimization procedure.

The Accelerated Process Optimization (APO), which is able to deal with single objective process optimization cases, is embedded in the proposed m-APO framework to jointly solve the constructed sub-problems. The APO leverages the experimental data from prior similar-but non-identical-processes to accelerate the optimization procedure in the current process [15]. The same idea is incorporated within m-APO by treating the experimental data from previous sub-problems as prior data for optimizing the current sub-problem at each stage.

After identifying the existing Pareto optimal solutions on the objective space at each step, m-APO intelligently constructs the best next sub-problem which has the most potential to efficiently improve the approximation of the Pareto front. Consequently, a large number of experimental runs will be saved by smartly selecting only a few subproblems to solve amongst an infinite number of them.

Moreover, in lieu of independently and separately designing experiments for optimizing each sub-problem, experimental data obtained from previews sub-problems are utilized as prior data in the APO framework to accelerate optimization process for the next sub-problems. Fig. 7 demonstrates an illustrative example of applying the m-APO approach to maximize parts' relative density and elongation-to-failure based on our initial experimental data. For example, in Fig. 7 experimental data from sub-problem 1 (represented by segments a-b-c) facilitates the

Fig. 5. Schematic illustration of design space, objective space, optimal design point, Pareto optimal solution and Pareto front [41,44].

<!-- image -->

Elongation-to-failure

Layer Thickness (mm)

Layer Thickness (mm)

1.0

0.0550

Estimated Pareto Front -

0.8

0.0525

0.6

0.0500

0.4

0.0475

0.2

a

0.0

0.0450

0.0550

0.3

0.0525

0.0500

0.0475

0.0450

0.145

Data from sub-problem 2

Data from sub-problem 3

Data from sub-problem 4

0.4

0.5

0.6

Density

0.150

0.155

Hatch Spacing (mm)

= 0.7

Fig. 6. Different combinations of weight coefficients lead to distinct shapes of contour plot for the weighted summation of part relative density and elongation-tofailure.

<!-- image -->

Fig. 7. The m-APO leverages experimental data obtained from prior sub-problems to accelerate solving the subsequent sub-problems (response values are scaled within [FRO] range).

<!-- image -->

optimization procedure for sub-problem 2. Hence, the algorithm can achieve the Pareto optimal solution corresponding to the sub-problem 2 (i.e., segment e) with fewer experimental trials. Similarly, the information captured by experimental data obtained from sub-problems 1, 2 and 3 (represented by segments a-b-c, d-e and f-g respectively) contribute to achieving the Pareto optimal solution corresponding to sub-problem 4 (i.e., segment h) by conducting only one experiment. m-APO leverages the prior experimental data to avoid individually designing the experiments for each sub-problem from scratch.

The m-APO continues this procedure till the improvement in the resulting Pareto front approximation is not significant. The magnitude of dominated area on the objective space is used to evaluate the efficiency of the resulting Pareto optimal solutions. The m-APO algorithm is described in detail in the Appendix A.

## 4. Experimental case study and discussion: mechanical properties optimization of Ti-6Al-4V parts fabricated by Selective Laser Melting (SLM)

Now we apply the m-APO to a real case study to maximize the relative density and elongation-to-failure of Ti-6Al-4 V parts fabricated by

SLM. Note that m-APO can be applied to optimize any conflicting couple of scalar mechanical properties for any LBAM-fabricated part with any material. The efficiency of m-APO is tested via a series of extensive simulation studies in the authors' previous studies [41-44]. Its robustness is also validated against test problems with different number of input process parameters and characteristics of objective space and Pareto fronts (including convex and non-convex Pareto fronts) [41-44]. Hence, in the present study we only present a real-world case study and benchmark the results against full factorial DOE. The results show that m-APO outperforms an extended full factorial DOE by 51.8% in terms of achieving the true Pareto front with fewer experimental runs.

## 4.1. Experimental data generation: fabrication and test procedures

Spherical gas atomized Grade 23 Ti-6Al-4 V (ASTM B348 - 13 [45]) powder was used in an argon-purged AM machine (Renishaw AM250) to fabricate the specimens. Chemical composition of the powder is reported in Table 1. Various combinations of process parameters were used in this study - mainly by varying the laser power, hatch spacing, and layer thickness - to fabricate the rods (see Section 4.2). Four rods were fabricated by using each set of process parameters at a time. All the rods were fabricated in the vertical direction and the scanning path was the same for all the fabricated rods.

Ti-6Al-4V rods of 7 mm diameter were fabricated using SLM machine on a Ti-6Al-4V build plate. After separation from the build plate, the fabricated bars were machined to a solid circular shape with straight gauge section of 3.6 mm diameter for tensile testing [46]. Before tensile testing, relative density of bars was measured and reported, considering Ti-6Al-4V wrought material density as the reference.

Geometry of the tensile specimens were designed according to the specifications of ASTM E-8 standard [46] and is indicated in Fig. 8.

Table 1 Chemical composition of powder used to fabricate the Ti-6Al-4 V specimens.

| Element            |   Al |    C |    Fe |      H |    N |    O | Ti      |   V | Others   |
|--------------------|------|------|-------|--------|------|------|---------|-----|----------|
| Weight percent (%) |  6.4 | 0.01 | 0.021 | 0.0029 | 0.02 | 0.11 | Balance | 4.1 | <0.4     |

e

(%)

Elongation-to-failure

5

22.5

4

2

1

,18

- Pareto front

Response data

1 ф 3.6

1 $7

Fig. 8. Schematic showing the dimensions of the specimen used in monotonic tensile tests (all dimensions are in mm).

<!-- image -->

Gauge section of the specimen was mechanically polished using SiC sandpaper to minimize the effects of surface condition on the mechanical response. Monotonic tensile tests were conducted in straincontrolled condition using an MTS 810 servo-hydraulic testing machine at a strain rate of 10 -3 s -1 . Elongation-to-failure and stress values such as ultimate and yield stress (if observable) were collected from tensile tests to be used for optimizing the process parameters.

## 4.2. Initial design of experiments setups and data generation

We applied full factorial DOE plans to generate experimental data forming our targeted design and objective spaces. Initially we designed a × % ) x w P8: ) full factorial DOE (see Table 2). The design space is originally centered on the process parameters setup recommended by SLM manufacturer for Ti-6Al-4 V. The increment for process parameters' levels are selected based on the LBAM system sensitivity to the process parameters and the availability of resources. After conducting and testing some experiments we observed that parts with the largest hatch spacing (i.e., 0.168 mm) are extremely prone to low elongation-tofailure as well as low failure stress. Hence, after making conducting and testing 3 sets of experiments with 0.168 mm hatch spacing, we replaced the hatch spacing of 0.168 mm with 0.144 mm for the rest of the experiments (see Table 3).

Moreover, to focus on the effect of laser power, we designed a × × % P x )w V: full factorial DOE plan-as an auxiliary design-including the laser power at the level of (see Table 3). Eventually, we conducted 27 sets of experiments each with 3 replications to generate a design and objective space. All the experimental data are presented in Appendix B.

## 4.3. Apply multi-objective accelerated process optimization (m-APO)

This section applies m-APO to efficiently maximize the relative density and elongation-to-failure of parts. The extended full factorial DOE plan presented in Section 4.2 results in a design and objective space with size of 27 including 6 Pareto optimal solutions (cross circles in Fig. 9). Starting from a random design point, we iteratively apply mAPO. We stop the optimization process at the 13 th experiment because we achieved the same 6 Pareto optimal solutions at this stage. Therefore, employing m-APO we attain the true Pareto front while saving 14 experimental runs, which means 51.8% experimental runs compared with our initial extended full factorial design.

Process parameter setups associated with the Pareto optimal solutions-along with the corresponding relative density, elongation-tofailure and ultimate strength-are presented in Table 4. In fact, we efficiently identified a set of process parameters resulting in the best

Table 2 Levels of the process parameters applied in the initial full factorial DOE plan. After conducting and testing some experiments hatch spacing of 0.168 mm is replaced with 0.144 mm.

| Laser power (W)      |   380 |      |                             |
|----------------------|-------|------|-----------------------------|
| Layer thickness (mm) | 0.045 | 0.05 | 0.055                       |
| Hatch spacing (mm)   | 0.152 | 0.16 | 0.168 (replaced with 0.144) |

Table 3 Levels of the process parameters applied in the auxiliary full factorial DOE plan to narrow down to the effect of laser power.

Fig. 9. Demonstrating the objective space, Pareto optimal solutions and conducted experiments by m-APO.

| Laser power (W)      |   390 |      |      |       |
|----------------------|-------|------|------|-------|
| Layer thickness (mm) | 0.045 | 0.05 |      | 0.055 |
| Hatch spacing (mm)   | 0.152 |      | 0.16 |       |

<!-- image -->

Optimal process parameters and the corresponding, relative density, elonga-

Table 4 tion-to-failure and ultimate stress.

|   Laser power (W) |   Layer thickness (mm) |   Hatch spacing (mm) |   Relative density |   4 w f |   G>a w u |
|-------------------|------------------------|----------------------|--------------------|---------|-----------|
|               380 |                  0.05  |                0.144 |             0.9839 |    2.22 |   1198.43 |
|               400 |                  0.05  |                0.144 |             0.9819 |    2.38 |   1226.97 |
|               400 |                  0.045 |                0.144 |             0.9722 |    4.84 |   1243.97 |
|               380 |                  0.045 |                0.144 |             0.9796 |    3.47 |   1224.4  |
|               400 |                  0.045 |                0.16  |             0.9797 |    2.82 |   1199.15 |
|               380 |                  0.055 |                0.144 |             0.9748 |    3.97 |   1250.57 |

compromises in terms of the relative density and tensile properties of parts while significantly reducing the number of required experimental runs. As can be seen in Fig. 9, there are many specimens - fabricated with different process parameters - that yield in a high relative density. However, the corresponding elongation-to-failure for those specimens is very low (see the data with relative density &gt; 0.97 and elongation-to-failure &lt; 2). The small elongation-to-failure for these specimens may be explained by the distribution of the void, as previously depicted in Fig. 1. In other words, for those specimens with high relative density, although there exists lower amount of fabrication-induced voids, these voids may have been huddled in some locations of the gauge section, resulting to a weak point on the gauge section and, subsequently, very small elongation-to-failure. This is in agreement with the observations in the literature regarding the higher effect of voids' distribution than the total amount of density on the fracture of AM metals [47-49]. Another reason, for these observations, could be the presence of the small-volume flat voids (i.e. un-melted regions) due to the lack-of-fusion for some cases [19,20]. Presence of un-melted regions in the LBAM specimens does not influence the relative density of the part, while resulting in a weak section along the specimen's length and, thus, premature failure of the corresponding specimens. That being said, the multi-objective accelerated process optimization (m-APO) employed in this study, can implicitly account for the effects of void type and distribution. As a result, it can efficiently achieve sets of process parameter setups- corresponding to the Pareto front of Figure 9- that not only fabricate parts with a high relative density, but also with an acceptable elongation-to-failure.

·z

0.0550

0.0525

0.0500

0.0475

0.0450

0.145

· 0.0550

0.0525

0.0500

0.0475

0.0450

0.145

Sub-Problem 1

V1 = 1,12=0

a

HV improvement, AHV

0.18

0.26

0.10

0.26

0.34

<!-- image -->

0.0525

Fig. 10. Schematic illustration of applying APO to different sub-problems, and representing the design space dynamics associated with conducting m-APO.

Fig. 11. Schematic illustration of HV as the yardstick of improving the Pareto front approximation. The black rectangle represents HV , i.e., the contribution of a new Pareto optimal solution with regard to HV improvement.

<!-- image -->

## 5. Conclusions

The present work proposed a novel approach to efficiently optimize different mechanical properties of LBAM-fabricated parts. The experimental data show that parts within an acceptable range of relative density possess very different magnitude of tensile mechanical properties (such as elongation-to-failure). In other words, different mechanical properties demonstrate nearly conflicting behavior in the optimal density window. The variation in the tensile mechanical properties of the specimens with almost similar relative density, although fabricated with different process parameters, could be attributed to the size and distribution of the fabrication-induced voids along the volume of the specimen (see Fig. 1). The applied multi-objective accelerated process optimization (m-APO) methodology is able to achieve a set of process parameter setups resulting in the best trade-off between conflicting mechanical properties of parts in the optimal regime (such as relative density and elongation-to-failure in Fig. 4).

The m-APO methodology separates the master multi-objective problem into a sequence of single-objective sub-problems and intelligently solves the subproblems with the highest chance to achieve the Pareto optimal solution, representing the best compromise between conflicting mechanical properties. At each stage, m-APO method leverages the experimental data generated from previous sub-problems to accelerate the optimization procedure of the remaining sub-problems.

The m-APO is applied to a real-world case study aimed at maximizing relative density and elongation-to-failure of Ti-6Al-4 V parts fabricated by SLM system. The m-APO method was able to achieve the optimal process parameter setups while reducing the experimental runs by 51.8% compared to an initial extended full factorial DOE. The mAPO method, which results in not only a high density, but also a satisfactory level of elongation-to-failure-as employed in this study-indirectly accounts for the effect of size and distribution of the voids on different mechanical properties of the fabricated parts.

## Acknowledgement

Research was sponsored by the Army Research Laboratory and was accomplished under Cooperative Agreement Number W911NF-15-20025. The views and conclusions contained in this document are those of the authors and should not be interpreted as representing the official policies, either expressed or implied, of the Army Research Laboratory or the U.S. Government. The U.S. Government is authorized to reproduce and distribute reprints for Government purposes notwithstanding any copyright notation herein.

Sub-Problem 2

Yi = 0,Yz = 1

&lt;

## Appendix A. Multi-Objective Accelerated Process Optimization (m-APO)

The algorithm of m-APO is described in detail as follows:

## Step 1: Decomposing master problem into sub-problems

First, the master bi-objective optimization problem is broken down into a sequence of single objective sub-problems formulated (solvable by APO) as a convex combination of individual objective functions represented by Eq. (2). To identify the scope of objective space, m-APO first requires achieving a targeted optimum value for individual objectives. (In our LBAM mechanical properties optimization case, the targeted value for part relative density and elongation-to-failure should be set considering the powder properties and the machine technical capabilities. Those should be reasonable desired values.) Hence, the algorithm is initialized by choosing two boundary sub-problems with = = , FR Ok O O x O and = = , OR Fk O x x x . These two initial sub-problems represent the single objective optimization problems with respect to only one mechanical property. The solution to the first two sub-problems identifies the ends of Pareto front on the objective space (i.e., segments e and c in Fig. 7)

## Step 2: Applying Accelerated Process Optimization (APO) to sub-problems

The APO [15] is incorporated into m-APO framework to consecutively design experiments and optimize the selected single objective subproblems at each step. Suppose the weight coefficients associated with the current sub-problem is already identified, i.e., h O and h x . All the design points and the corresponding response vectors, i.e., ( s Y R i i ), are mapped and scaled to the current sub-problem in the form of weighted summation of single responses, i.e., ( s Z j i i h ) via the transformation equation = + s s s Z Y Y ( ) . ( ) . ( ) i h i h i h i 1 1 2 2 represented by Eq. (2). The experimental data obtained from optimization procedure of previous sub-problems (i.e., sub-problems … h Pj)j j P ) are treated as prior data and fed into APO to guide and accelerate optimization of the current sub-problem (i.e., h th sub-problem). APO leverages the transformed information to improve prediction of the weighted single objective responses corresponding to the untested design points for the subsequent sub-problems. Consequently, improving the prediction accuracy of the single objective responses result in guiding the algorithm towards achieving the Pareto optimal solution corresponding to the current sub-problem in an accelerated manner.

APO makes a direct analogy with a fundamental electrostatic law to balance optimization and space-filling properties. In any sub-problem APO assigns a simulative positive charged particle s q w : h j to each design point. The charge function s q w : h should be appropriately selected in relation to the objective of optimization. Since our case is a maximization problem, s q w : h should be defined as an inversely proportional function of the weighted single objective response values s Z w : h corresponding to each sub-problem in Eq. (2) [15,50]. Considering this, particles with lower charge are assigned to design points with higher s Z w : h and converse. Fig. 10 demonstrates an illustrative example of applying APO and the associated dynamics in the design space corresponding to the objective space illustrated in Fig. 7. For instance, design points (a) and (b) on the right side of Fig. 10 (a) are illustrated with larger positive particles compared with design point (c) on the middle left of the contour plot. This is because of the fact that design points (a) and (b) result in lower Z O in comparison with design point (c). Note that, since the combination of weight coefficients and the corresponding single objective response values s Z w : h changes from one sub-problem to another, the corresponding charge function should change as well. Hence, we observe that positive particle charges with different sizes are assigned to the same design points in different contour plots (i.e., different sub-problems). m-APO leverages the dynamics associated with the differences amongst the sub-problems' objective spaces by intelligently mapping the charged particles from one sub-problem to another. Similar to a fundamental electrostatic law, the design points (so-called positive charged particles) push each other apart so as to minimize the total electrostatic potential energy in the contour plot domain (i.e., design space). Since the design points associated with the lower charged particles (i.e., with higher s Z w : h ) weakly repel others, more new design points have the chance to be accommodated in their neighborhood. The resulting allocation of the design points corresponds to the minimum total potential energy. Considering this analogy, the sequential selection of the design points will lead to maximize the objective function of interest in the current sub-problem (i.e., s Z w : h ) with reduced number of experimental runs.

The so-called electrostatic potential energy between any two design points s i and s j is defined as s s s s q q d w : w :z w j : i j i j , where s s d w j : i j represents the Euclidean distance between s i and s j. Therefore, the total electrostatic potential energy function corresponding to the h th sub-problem including the n th new design is formulated as follows:

<!-- formula-not-decoded -->

The new design point can be obtained by solving = s argmin E n n h . Details of the single objective response value prediction for new untested design points and the charge function computation is beyond the scope of the present paper and can be found in Ref. [15].

## Step 3: Defining Hyper-Volume (HV) and stopping criteria for sub-problems

Hyper-Volume ( HV ) metric-a well-known performance indicator in the realm of multi-objective optimization-is employed to construct the stopping criteria for m-APO [51,52]. HV assesses the size of the region on the objective space dominated by the resulting Pareto optimal solutions. Therefore, higher HV indicates better coverage of the true Pareto front and thus bring about the better Pareto front approximation. Throughout the algorithm, HV (i.e., HV increment) represents the contribution of a new Pareto optimal solution in terms of solution improvement. In other words, HV quantifies the achievement of a new Pareto optimal solution. For instance, in Fig. 11 black rectangle represents HV associated with a new Pareto optimal solution. Moreover, the size of the whole shaded area (including the black rectangle) indicates the HV associated with the current approximated Pareto front. m-APO continues designing experiments for the current sub-problem via APO until the current HV is less than a prespecified boundary &lt; i e -' w 2 2 j : P . In that case, m-APO stops proceeding with the current sub-problem and move on to the next sub-problem. Moreover, m-APO stops keep constructing new sub-problems and consequently designing more experiments when a significant improvement in HV is not observed &lt; i e -' w 2 2 j : ) .

## Step 4: Constructing sub-problems by determining appropriate weight coefficients

At the end of each sub-problem, contingent upon the distribution of the current Pareto optimal solutions, m-APO calculates the appropriate weight coefficients (i.e., h ) to construct the next sub-problem. The weighting coefficients are identified in a way to cover the existing gaps on the Pareto front. Note that in the preset work unknown variables are represented by upper case letters, while known variables are illustrated by lower case letters. Suppose m-APO stopped designing experiments for the h , Ok th sub-problem. Hence, currently m optimal design points and corresponding Pareto optimal solutions are achieved represented by the set = … s y s y s y {( , ), ( , ), , ( , )} * * * * * * h m m 1 1 1 2 2 . Afterwards, the Euclidean distance between all of the neighboring Pareto points and accordingly the largest gap on the existing Pareto front is determined as follows:

<!-- formula-not-decoded -->

= = … max j m j w) ) V wS

Suppose s 1 a and s 1 b are the neighboring Pareto points corresponding to , where &lt; s s y y ( ) ( ) * * a b 1 1 . To cover the largest gap on the existing Pareto front, the weight coefficients for the next sub-problem is identified as = s s s s c y y y y ( ( ) ( ) , ( ) ( )) * * * * h h a b b a 2 2 1 1 , where c h is a constant leading to O = O h h O x . In that way, the consecutive sub-problems can efficiently achieve well-distributed Pareto optimal points to approximate the true Pareto front using minimum amount of resource.

## Appendix B. Experimental Data Table

|   Laser power (W) |   Layer thickness (mm) |   Hatch spacing (mm) |   Relative density |   wL: f |
|-------------------|------------------------|----------------------|--------------------|---------|
|               380 |                  0.05  |                0.144 |               4.36 |    2.13 |
|                   |                        |                      |               4.38 |    1.45 |
|                   |                        |                      |               4.34 |    3.08 |
|               380 |                  0.05  |                0.152 |               4.33 |    1.39 |
|                   |                        |                      |               4.3  |    2.88 |
|                   |                        |                      |               4.31 |    1.68 |
|               380 |                  0.05  |                0.16  |               4.25 |    0.88 |
|                   |                        |                      |               4.28 |    0.85 |
|                   |                        |                      |               4.31 |    1.32 |
|               400 |                  0.05  |                0.144 |               4.34 |    2.67 |
|                   |                        |                      |               4.35 |    2.7  |
|                   |                        |                      |               4.36 |    1.78 |
|               400 |                  0.045 |                0.144 |               4.35 |    5.22 |
|                   |                        |                      |               4.28 |    4.91 |
|                   |                        |                      |               4.29 |    4.4  |
|               400 |                  0.055 |                0.144 |               4.3  |    2.66 |
|                   |                        |                      |               4.32 |    1.56 |
|                   |                        |                      |               4.33 |    1.19 |
|               380 |                  0.045 |                0.144 |               4.35 |    4.36 |
|                   |                        |                      |               4.34 |    2.17 |
|                   |                        |                      |               4.33 |    3.87 |
|               380 |                  0.045 |                0.152 |               4.36 |    2.14 |
|                   |                        |                      |               4.35 |    1.58 |
|                   |                        |                      |               4.35 |    2.22 |
|               380 |                  0.045 |                0.16  |               4.31 |    1.1  |
|                   |                        |                      |               4.28 |    1.4  |
|                   |                        |                      |               4.33 |    0.89 |
|               390 |                  0.045 |                0.152 |               4.26 |    1.19 |
|                   |                        |                      |               4.29 |    2.3  |
|                   |                        |                      |               4.37 |    2.1  |
|               390 |                  0.045 |                0.16  |               4.3  |    1.07 |
|                   |                        |                      |               4.3  |    1.16 |
|                   |                        |                      |               4.31 |    0.81 |
|               390 |                  0.055 |                0.152 |               4.35 |    2.5  |
|                   |                        |                      |               4.36 |    1.04 |
|                   |                        |                      |               4.36 |    2.05 |
|               390 |                  0.055 |                0.16  |               4.29 |    1.12 |
|                   |                        |                      |               4.37 |    0.98 |
|                   |                        |                      |               4.17 |    0.73 |
|               390 |                  0.05  |                0.152 |               4.38 |    1.41 |
|                   |                        |                      |               4.33 |    1.28 |
|                   |                        |                      |               4.3  |    1.11 |
|               390 |                  0.05  |                0.16  |               4.29 |    0.93 |
|                   |                        |                      |               4.2  |    0.62 |
|                   |                        |                      |               4.52 |    1.1  |

|   400 |   0.05 |   0.16 |   4.29 |   1.96 |
|-------|--------|--------|--------|--------|
|       |        |        |   3.77 |   4.37 |
|       |        |        |   4.33 |   1.32 |
|   400 |  0.045 |  0.168 |   4.3  |   1.15 |
|       |        |        |   4.19 |   0.81 |
|       |        |        |   4.18 |   0.76 |
|   400 |  0.05  |  0.168 |   4.32 |   1.16 |
|       |        |        |   4.26 |   0.89 |
|       |        |        |   4.33 |   1.52 |
|   400 |  0.045 |  0.152 |   4.33 |   2.14 |
|       |        |        |   4.16 |   0.27 |
|       |        |        |   4.38 |   2.48 |
|   400 |  0.05  |  0.152 |   4.36 |   1.59 |
|       |        |        |   4.36 |   1.91 |
|       |        |        |   4.34 |   0.68 |
|   400 |  0.045 |  0.16  |   4.36 |   2.71 |
|       |        |        |   4.34 |   2.82 |
|       |        |        |   4.31 |   2.94 |
|   400 |  0.055 |  0.152 |   4.36 |   2.9  |
|       |        |        |   4.29 |   2.6  |
|       |        |        |   4.33 |   2.9  |
|   400 |  0.055 |  0.168 |   4.2  |   0.6  |
|       |        |        |   4.22 |   0.9  |
|       |        |        |   4.16 |   0.8  |
|   400 |  0.055 |  0.16  |   4.32 |   0.7  |
|       |        |        |   4.32 |   2.6  |
|       |        |        |   4.39 |   1.65 |
|   380 |  0.055 |  0.144 |   4.29 |   1.6  |
|       |        |        |   4.33 |   3.3  |
|       |        |        |   4.34 |   7    |
|   380 |  0.055 |  0.16  |   4.27 |   1.4  |
|       |        |        |   4.29 |   0.7  |
|       |        |        |   4.29 |   1.1  |
|   380 |  0.055 |  0.152 |   4.32 |   2.1  |
|       |        |        |   4.31 |   1.7  |
|       |        |        |   4.32 |   1.7  |

## References

- [1] Murr LE, Gaytan SM, Medina F, Lopez H, Martinez E, Machado BI, Hernandez DH, Martinez L, Lopez MI, Wicker RB, Bracke J. Next-generation biomedical implants using additive manufacturing of complex, cellular and functional mesh arrays. Philos Trans R Soc Lond A: Math Phys Eng Sci 2010;368(1917):1999-2039.
- [2] Niinomi M. Mechanical biocompatibilities of titanium alloys for biomedical applications. J Mech Behav Biomed Mater 2008;1(1):30-42.
- [3] Elias CN, Lima JHC, Valiev R, Meyers MA. Biomedical applications of titanium and its alloys. JOM 2008;60(3):46-9.
- [4] Rack HJ, Qazi JI. Titanium alloys for biomedical applications. Mater Sci Eng C 2006;26(8):1269-77.
- [5] Matassi F, Botti A, Sirleo L, Carulli C, Innocenti M. Porous metal for orthopedics implants. Clin Cases Miner Bone Metab 2013;10(2):111-5.
- [6] Vasconcellos L, Leite D, Nascimento F, Vasconcellos LG, Graca M, Carvalho Y, et al. Porous titanium for biomedical applications: an experimental study on rabbits. Med Oral Patol Oral Y Cir Bucal 2010:e407-12.
- [7] TAKAHASHI M, KIKUCHI M, TAKADA Y. Mechanical properties and microstructures of dental cast Ti-Ag and Ti-Cu alloys. Dent Mater 2002.
- [8] Al-Mayouf A, Al-Swayih A, Al-Mobarak N, Al-Jabab A. Corrosion Behavior of a New Titanium Alloy for Dental Implant Applications in Fluoride Media. Mater Chem Phys 2004;86(2-3):320-9.
- [9] Boyer R. An overview on the use of titanium in the aerospace industry. Mater Sci Eng A 1996;213(1):103-14.
- [10] Peters M, Kumpfert J, Ward CH, Leyens C. Titanium Alloys for Aerospace Applications. Adv Eng Mater 2003;5(6):419-27.
- [11] Leyens C Christoph, Peters M Manfred. Titanium and titanium alloys : fundamentals and applications Wiley-VCH. John Wiley &amp; Sons., and Wiley InterScience (Online service); 2003.
- [12] Tung SC, McMillan ML. Automotive tribology overview of current advances and challenges for the future. Tribol Int 2004;37(7):517-36.
- [13] Sachdev AK, Kulkarni K, Fang ZZ, Yang R, Girshov V. Titanium for automotive applications: challenges and opportunities in materials and processing. JOM 2012;64(5):553-65.
- [14] Aboutaleb AM, Bian L. Optimization of laser-based additive manufacturing,' laserbased additive manufacturing of metal parts: modeling, optimization, and control of mechanical properties. CRC Press, Taylor &amp; Francis Group; 2017. p. 137-60.
- [15] Aboutaleb AM, Bian L, Elwany A, Shamsaei N, Thompson SM, Tapia G. Accelerated process optimization for laser-based additive manufacturing by leveraging similar prior studies. IIE Trans 2016;49(1):1-14.
- [16] Gong H, Rafi K, Gu H, Starr T, Stucker B. Analysis of defect generation in Ti-6Al-4V parts made using powder bed fusion additive manufacturing processes. Addit Manuf 2014;1-4:87-98.
- [17] Rafi HK, Karthik NV, Gong H, Starr TL, Stucker BE. Microstructures and mechanical properties of Ti6Al4V parts fabricated by selective laser melting and Electron beam melting. J Mater Eng Perform 2013;22(12):3872-83.
- [18] Effects of defects in laser additive manufactured Ti-6Al-4V on fatigue properties. Phys Procedia 2014;56:371-8.
- [19] Yadollahi A, Shamsaei N. Additive manufacturing of fatigue resistant materials: challenges and opportunities. Int J Fatigue 2017;98:14-31.
- [20] Bagheri A, Mahtabi MJ, Shamsaei N. Fatigue behavior and cyclic deformation of additive manufactured NiTi. J Mater Process Technol 2017.
- [21] Leuders S, Thöne M, Riemer A, Niendorf T, Tröster T, Richard HA, et al. On the mechanical behaviour of titanium alloy TiAl6V4 manufactured by selective laser melting: fatigue resistance and crack growth performance. Int J Fatigue 2013;48:300-7.
- [22] Shamsaei N, Yadollahi A, Bian L, Thompson SM. An overview of direct laser deposition for additive manufacturing; Part II: mechanical behavior, process parameter optimization and control. Addit Manuf 2015;8:12-35.
- [23] Deshpande S, Watson LT, Canfield RA. Pareto front approximation using a hybrid approach. Procedia Comput Sci 2013;18:521-30.
- [24] Utyuzhnikov sv, Fantini P, Guenov MD. A method for generating a well-distributed pareto set in nonlinear multiobjective optimization. J Comput Appl Math 2009;223(2):820-41.
- [25] Eichfelder G. Adaptive scalarization methods in multiobjective optimization. Berlin, Heidelberg: Springer Berlin Heidelberg; 2008.
- [26] Abraham A, Jain L. Evolutionary multiobjective optimization, evolutionary multiobjective optimization. London: Springer-Verlag; 2005. p. 1-6.
- [27] Collette Y, Siarry P. Multiobjective optimization: principles and case studies. Berlin, Heidelberg, New York: Springer; 2003.
- [28] Deb D. Multi-objective optimization using evolutionary algorithms. Chichester: J. Wiley &amp; Sons; 2001.
- [29] Deb K, Pratap A, Agarwal S, Meyarivan T. A fast and elitist multiobjective genetic algorithm: NSGA-II. IEEE Trans Evol Comput 2002;6(2):182-97.
- [30] Hrabe N, Quinn T. Effects of processing on microstructure and mechanical

properties of a titanium alloy (Ti-6Al-4V) fabricated using Electron beam melting (EBM), part 2: energy input, orientation, and location. Mater Sci Eng A 2013;573:271-7.

- [31] Selcuk C. Laser metal deposition for powder metallurgy parts. Powder Metall. 2011;54(2):94-9.
- [32] Simonelli M, Tse YY, Tuck C. Effect of the build orientation on the mechanical properties and fracture modes of SLM Ti-6Al-4V. Mater Sci Eng A 2014;616:1-11.
- [33] Wauthle R, Vrancken B, Beynaerts B, Jorissen K, Schrooten J, Kruth JP, et al. Effects of build orientation and heat treatment on the microstructure and mechanical properties of selective laser melted Ti6Al4V lattice structures. Addit Manuf 2015;5:77-84.
- [34] Carroll BE, Palmer TA, Beese AM. Anisotropic tensile behavior of Ti-6Al-4V components fabricated with directed energy deposition additive manufacturing. Acta Mater 2015;87:309-20.
- [35] Baufeld B, Biest O Vander, Gault R. Additive Manufacturing of Ti-6Al-4V Components by Shaped Metal Deposition: Microstructure and Mechanical Properties. Mater Des 2010;31(SUPPL. 1):S106-11.
- [36] Wang Y, Zhang S, Tian X, Wang H. High-cycle fatigue crack initiation and propagation in laser melting deposited TC18 titanium alloy. Int J Miner Metall Mater 2013;20(7):665-70.
- [37] Yadollahi A, Mahtabi MJ, Khalili A, Doude HR, Newman Jr JC. Fatigue life prediction of additively manufactured material: effects of surface roughness, defect size, and shape. Fatigue Fract Eng Mater Struct 2018;41(7):1602-14.
- [38] Silva ACF, Braga DFO, de Figueiredo MAV, Moreira PMGP. Ultimate tensile strength optimization of different FSW aluminium alloy joints. Int J Adv Manuf Technol 2015;79(5-8):805-14.
- [39] Bozkurt Y. The optimization of friction stir welding process parameters to achieve maximum tensile strength in polyethylene sheets. Mater Des 2012;35:440-5.
- [40] Ampaiboon A, Lasunon OU, Bubphachot B. Optimization and prediction of ultimate tensile strength in metal active gas welding. Sci World J 2015;2015.
- [41] Aboutaleb AM, Tschopp MA, Rao PK, Bian L. Multi-objective accelerated process optimization of part geometric accuracy in additive manufacturing. J Manuf Sci Eng

2017.

- [42] Aboutaleb AM, Bian L, Shamsaei N, Thompson SM. Systematic optimization of laser-based additive manufacturing for multiple mechanical properties. 2016 IEEE International Conference on Automation Science and Engineering (CASE), IEEE; 2016. p. 780-5.
- [43] Aboutaleb AM, Bian L, Shamsaei N, Thompson SM, Rao PK. Multi-objective process optimization of additive manufacturing: a case study on geometry accuracy optimization. Proceedings of the Annual International Solid Freeform Fabrication Symposium. 2016. p. 656-69.
- [44] Aboutaleb AM, Bian L, Rao PK, Tschopp MA. Accelerated geometry accuracy optimization of additive manufacturing parts. ASME 12th International Manufacturing Science and Engineering Conference. 2017.
- [45] ASTM B348-13, Standard Specification for Titanium and Titanium Alloy Bars and Billets. West Conshohocken, PA: ASTM International; 2013. Www.astm.org.
- [46] ASTM E8 / E8M-13, Standard Test Methods for Tension Testing of Metallic Materials. West Conshohocken, PA: ASTM International; 2013. Www.astm.org.
- [47] Thompson A, Maskery I, Leach RK. X-ray computed tomography for additive manufacturing: a review. Meas Sci Technol 2016;27(7):72001.
- [48] Siddique S, Imran M, Rauer M, Kaloudis M, Wycisk E, Emmelmann C, et al. Computed tomography for characterization of fatigue performance of selective laser melted parts. Mater Des 2015;83:661-9.
- [49] Carlton HD, Haboub A, Gallegos GF, Parkinson DY, MacDowell AA. Damage evolution and failure mechanisms in additively manufactured stainless steel. Mater Sci Eng A 2016;651:406-14.
- [50] Dasgupta T. Robust parameter design for automatically controlled systems and nanostructure synthesis. Georgia Institute of Technology; 2007.
- [51] Knowles J. ParEGO: a hybrid algorithm with on-line landscape approximation for expensive multiobjective optimization problems. IEEE Trans Evol Comput 2006;10(1):50-66.
- [52] Zitzler E, Thiele L, Laumanns M, Fonseca CM, da Fonseca VG. Performance assessment of multiobjective optimizers: an analysis and review. IEEE Trans Evol Comput 2003;7(2):117-32.