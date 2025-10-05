# Metadata:
**Title:** pyCycle: A Tool for Efficient Optimization of Gas Turbine Engine Cycles
**Authors:** [[Eric S. Hendricks]], [[Justin S. Gray]]
**Year:** 2019
**CiteKey**: Hendricks2019_pyCycleToolEfficient
**Zotero_Link**: zotero://select/items/@Hendricks2019_pyCycleToolEfficient
**URL**: https://www.mdpi.com/2226-4310/6/8/87


# Abstract
Aviation researchers are increasingly focusing on unconventional vehicle designs with tightly integrated propulsion systems to improve overall aircraft performance and reduce environmental impact. Properly analyzing these types of vehicle and propulsion systems requires multidisciplinary models that include many design variables and physics-based analysis tools. This need poses a challenge from a propulsion modeling standpoint because current state-of-the-art thermodynamic cycle analysis tools are not well suited to integration into vehicles level models or to the application of efficient gradient-based optimization techniques that help to counteract the increased computational costs. Therefore, the objective of this research effort was to investigate the development a new thermodynamic cycle analysis code, called pyCycle, to address this limitation and enable design optimization of these new vehicle concepts. This paper documents the development, verification, and application of this code to the design optimization of an advanced turbofan engine. The results of this study show that pyCycle models compute thermodynamic cycle data within 0.03% of an identical Numerical Propulsion System Simulation (NPSS) model. pyCycle also provides more accurate gradient information in three orders of magnitude less computational time by using analytic derivatives. The ability of pyCycle to accurately and efficiently provide this derivative information for gradient-based optimization was found to have a significant benefit on the overall optimization process with wall times at least seven times faster than using finite difference methods around existing tools. The results of this study demonstrate the value of using analytic derivatives for optimization of cycle models, and provide a strong justification for integrating derivatives into other important engineering analyses.

# My Notes
- [[PyCycle]] is a [[Cycle Code]], similar to [[NPSS]]
- It was developed because tools like NPSS only consider the engine, PyCycle is a move towards "vehicle-based" optimization for modern concepts where the aircraft design and propulsion system are highly coupled, examples include [[Boundary Layer Ingestion]] and [[Turboelectric]] concepts.
- Build on the [[OpenMDAO]] optimization framework
- Key difference: uses analytical/hand calculated derivatives for most things, while this is a pain to set up probably, it is far more accurate and much faster (7-15x faster than NPSS). 

# The Op-Ed
- While I don't really care so much about speed and extreme accuracy, and I would rather use a finite-difference or some simpler and less error-prone method (like NPSS) to solve cycles, the great thing is pyCycle is **free and open-source** - very much unlike NPSS.

# Follow ups:
- [[ ]]

# Reference
[@Hendricks2019_pyCycleToolEfficient]
