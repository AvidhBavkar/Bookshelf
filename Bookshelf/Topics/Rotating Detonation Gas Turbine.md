One challenge is [[RDC Unsteady Pressure]], and how it interacts with turbomachinery:

[[RDC Unsteady Pressure Damping via Turbomachinery]], see that page for more info but it looks like really only the first stage has to deal with it.


## Turbines:
#### Efficiency Metrics
**Problem w/ Standard Isentropic Efficiency in PGC**:
Here's the equation for isentropic turbine efficiency:
![[Pasted image 20251016194324.png]]
But **in a PGC, the pressure and temperature are both temporally and spatially very unsteady**, so this definition can be tricky.

See this discussion in [[Rankin2017_OverviewPerformanceApplication]]:
*“First, the isentropic efficiency was calculated using the average temperatures before and after each of the turbine stages as well as the average pressure ratio. The application of this method to the RDE combustor is challenging in practice because the pressure ratio varies by up to 20%. There was significant circumferential variation in the temperature at each axial measurement location, for both the OEMC and the RDE. Using the average of the temperature measurements at each axial position resulted in nonphysical component efficiencies.”* (Rankin et al., 2017, p. 140)

Similarly, [[Rasheed2011_ExperimentalInvestigationsPerformance]] used the standard definition of turbine efficiency (kind of):
![[Pasted image 20251016194637.png]]
but they had an 8 point uncertainty on turbine efficiency. In their words:
*“A propagation of uncertainty analysis of the preceding equations showed that the turbine inlet temperature had a strong effect on the uncertainty of the turbine performance” (Rasheed et al., 2011, p. 5)*

**Instead:**
[[Rankin2017_OverviewPerformanceApplication]] proposed using the [[Turbine Factor]], which is defined as the energy extracted by the turbines : chemical energy into the system. In their rig, the factor was defined like this:
![[Pasted image 20251016195056.png]]
(It was a turboshaft so the numerator is the HPT power (compressor) + LPT power (turbine))
#### Survivability/Structural
In [[Rankin2017_OverviewPerformanceApplication]], the AFRL T63 RDC integrated turboshaft, the turbine showed no visible signs of damage after more than 20 minutes (cumulative) of operation.






