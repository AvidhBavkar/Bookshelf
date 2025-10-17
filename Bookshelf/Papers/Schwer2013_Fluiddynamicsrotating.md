# Summary
*Numerical study comparing H2-Air RDEs to Hydrocarbon-Air/Oxygen. The Hydrocarbons examined were Hydrogen, Ethylene, Ethane, and Propane. The finding was that there's no different thermo/fluid dynamics that preclude using ideal detonation models as a predictor for RDC performance, and that H2-Air results should extrapolate to other hydrocarbons as well*
*****
# Metadata:
Title: Fluid dynamics of rotating detonation engines with hydrogen and hydrocarbon fuels
Authors: Douglas Schwer, K. Kailasanath
Year: 2013
CiteKey: Schwer2013_Fluiddynamicsrotating
Zotero_Link: zotero://select/items/@Schwer2013_Fluiddynamicsrotating
URL: https://www.sciencedirect.com/science/article/pii/S1540748912000478
### Tags:
#Numerical #PGC 

# Abstract
Rotating detonation engines (RDE’s) represent a logical step from pulsed detonation engine concepts to a continuous detonation engine concept for obtaining propulsion from the high efficiency detonation cycle. The hydrogen/air and hydrogen/oxygen RDE concepts have been most extensively studied, however, being able to use hydrocarbon fuels is essential for practical RDE’s. The current paper extends our hydrogen/air model to hydrocarbon fuels with both air and pure oxygen as the oxidizer. Before beginning the RDE calculations, several detonation tube results are summarized showing the ability of the code to reproduce the correct detonation velocity and CJ properties. In addition, a calculation capturing the expected irregular detonation cell patterns of ethylene/air is also shown. To do the full range of fuels and oxidizers, we found the use of temperature-dependent thermodynamic properties to be essential, especially for hydrocarbon/oxygen mixtures. The overall results for air-breathing RDE’s with hydrocarbons ranged from 1990 to 2540s, while in pure oxygen mode the specific impulse varied from 700 to 1070s. These results were between 85% and 89% of the expected ideal detonation cycle results, and are in line with previous hydrogen/air estimates from our previous work. We conclude from this that hydrocarbon RDE’s are viable and that the basic flow-field patterns and behaviors are very similar to the hydrogen/air cases detailed previously.

# Goal/Question
- Past work on RDEs has largely been hydrogen-air or ethylene-air/oxygen. Is the fluid dynamics of hydrocarbon fueled RDE's significantly different than H2-Air RDEs, and can we extrapolate [[H2-Air]] findings to hydrocarbon RDEs? 

# Methodology
* Numerical study
	* Premixed fuel-air coming from a plenum
	* 2D Domain, unrolled RDC.
	* ID: 80mm
	* OD: 100mm
	* L: 100mm
	* Gap: 10mm
	* Plenum pressure: 10 ATM 300K
	* Injector Throat Area : Injector Face Area: 0.2
	* 1 bar backpressure
* Numerical [[Detonation Tube]] also simulated
	* Cool picture:
	* ![[Pasted image 20251016204638.png]]
* Limitations to the "induction time" model used:
	* Does not capture deflagration/diffusion burning
	* Assumed frozen flow past the det wave
	* No heat loss
* Compared 4 fuels all stoichiometric
	* [[Hydrogen-Air]]
	* [[Ethylene-Air]]
	* [[Ethylene-Oxygen]]
	* [[Propane-Air]]
	* [[Propane-Oxygen]]
	* [[Ethane-Air]]
	* [[Ethane-Oxygen]]
	* No Hydrogen-Oxygen: was just too reactive and unstable to converge
# Results
-![[Pasted image 20251016205706.png]]
See the ISPf vs Th.ISPf columns:
Ranges from 88% to 89.9% of the ideal detonation cycle for air based cycles.
These are upper limits on the efficiency, as "some of the loss mechanisms in a real RDE are not represented here"

# Conclusions
- Most of the differences in specific impulse between the fuels is due to the thermodynamics of the different fuels, and not the fluid dynamics of the RDE system
- “moving from hydrogen to hydrocarbon fuels should provide performance that can be predicted by the ideal detonation cycle” (Schwer and Kailasanath, 2013, p. 1998)
- “these results show that there is no inherent difficulty in switching from hydrogen/air to hydrocarbon/air” (Schwer and Kailasanath, 2013, p. 1998)
- “the behavior of RDE’s is not affected by the different thermodynamics of hydrocarbon fuels as opposed to hydrogen fuel, and the ideal detonation cycle remains a good baseline for the expected performance of the RDE” (Schwer and Kailasanath, 2013, p. 1998)

# The Op-Ed
- An important nothing burger: ideal detonation cycles are a good baseline for RDC performance, not just for H2-Air rdes but for hydrocarbons too.

# Follow-Ups
- [7-10] Hydrogen-Air RDE aspects:
	- Pressure effects
	- Engine sizing
	- Inlet effects on performance
	- Flow-field descriptions

# Reference
[@Schwer2013_Fluiddynamicsrotating]
