# Summary
*Review of RDE work at AFRL, speaks on chemiluminescence, RDC chamber design guidelines and impact on performance, nozzle/backpressure importance, and finally an integration of an RDC with a T-63 gas turbine. The results of the T-63 test are very promising, equal to or better than the deflagrative combustor when looking at Turbine Factor*
*****
# Metadata:
Title: Overview of Performance, Application, and Analysis of Rotating Detonation Engine Technologies
Authors: [[Brent A. Rankin]], [[Matthew L. Fotia]], [[Andrew G. Naples]], [[Christopher A. Stevens]], [[John L. Hoke]], [[Thomas A. Kaemming]], [[Scott W. Theuerkauf]], [[Frederick R. Schauer]]
Year: 2017
CiteKey: Rankin2017_OverviewPerformanceApplication
Zotero_Link: zotero://select/items/@Rankin2017_OverviewPerformanceApplication
URL: https://arc.aiaa.org/doi/10.2514/1.B36303
### Tags:
#PGC #Review_Paper
[[Pressure Gain Combustion]]
[[Rotating Detonation Gas Turbine]] 
# Abstract
Recent accomplishments related to the performance, application, and analysis of [[Rotating Detonation]] engine technologies are discussed. The pioneering development of [[Optically Accessible Rotating Detonation]] engines coupled with the application of established diagnostic techniques is enabling a new research direction. In particular, OH [[Chemiluminescence]] images of detonations propagating through the annular channel of a rotating detonation engine are reported and appear remarkably similar to computational fluid dynamic results of rotating detonation engines published in the literature. Specific impulse measurements of rotating detonation engines and pulsed detonation engines are shown to be quantitatively similar for engines operating on hydrogen/air and ethylene/air mixtures. The encouraging results indicate that rotating detonation engines are capable of producing thrust with fuel efficiencies that are similar to those associated with pulsed detonation engines while operating on gaseous hydrocarbon fuels. A rotating detonation engine is coupled with a turboshaft engine for the first time. The performance of the rotating detonation engine gas turbine engine **is similar to or better than that of the conventional gas turbine engine across a broad range of operating conditions**. Realizing the advantages of pressure gain combustion in rotating detonation engines is enabling new combustion system design opportunities and supporting the development of efficient and sustainable power and propulsion technologies.

# Scope
- Summary of recent work done at [[U.S. Air Force Research Laboratory]] related to RDEs (circa 2017). Several subparts:
	- 1: Review of Prior RDE work
	- 2: Images of detonations propagating are analyzed
	- 3: Performance of [[H2-Air]] and [[Ethylene-Air]] RDCs are measured
	- 4: Experimental Integration with a gas turbine
# Notes:
- Detonation wave height is primarily determined by stagnation pressure, while overall pressure affected predominantly by pressure ratio - 8 (2D Numerical!)
- [[Detonation Wall Curvature]]:
	- “detonation wave near the concave wall (convergent) is stronger than near the convex wall (divergent)” (Rankin et al., 2017, p. 132) -19
	- “The critical condition for detonations to propagate through the rectangular cross-section channel occurred when the radii of curvature of the inside wall were approximately 14–40 times the cell width” (Rankin et al., 2017, p. 132)
- The major processes that affect the flow are the:
	- 1) Detonation Combustion
	- 2) Deflagration Combustion (Parasitic)
	- 3) Secondary Shock
	- 4) Mixing
![[Pasted image 20251016173025.png]]
Deflagration vs Detonation:
![[Pasted image 20251016173422.png]]
### 2: AFRL Optically Accessible RDE Chemiluminescence
Dimensions given in the paper
![[Pasted image 20251016173543.png]]
Lit by a H2-Gox [[predetonator]]
[[slot-orifice injector]]

### 3: Operation/Performance of H2-Air and Ethylene-Air RDCs:
![[Pasted image 20251016175321.png]]
Air Injection Area Ratio: Air Injector / RDE Chamber = 0.435
Nozzle convergence ratio: Nozzle / RDE Chamber = 0.6

**Specific Thrust increases w/ mass-flow due to: Increased Initial Pressure of reactants + Increased backpressure**
![[Pasted image 20251016174658.png]]
Specific Thrust: $$=T/\dot{m_{air}}$$
Specific Impulse = $$T/\dot{m_{fuel}}$$
So idk why you would care about specific thrust that much (air is free!)

Influence of [[Detonation Channel Width]] on ISP:
![[Pasted image 20251016174953.png]]
Vertical shifting theorized to be caused by 3D effects:
- propellant mixing
- flow recirculation losses at base of channel (its like a backward facing step kinda thing)
- changes in "radial length scale" across the channel (idk what that means)

Comparison of [[Pulse Detonation Combustor]] and [[Rotating Detonation]] Specific Impulses for [[H2-Air]] and [[Ethylene-Air]] show great agreement:
![[Pasted image 20251016175934.png]]
[[Rotating Detonation Nozzles]]:
I wasn't super interested, so read more in depth if you care:
![[Pasted image 20251016180108.png]]
![[Pasted image 20251016180320.png]]
Choking the nozzle is good: backpressures the combustor which makes it work better.
“choked aerospike indicated that there was **additional performance to be realized with additional choking of the flow beyond the thermal choke present in the detonation channel**.” (Rankin et al., 2017, p. 138)
“result suggests that the **unsteady exhaust from the RDE does not create unforeseen issues** with respect to flowing the exhaust through a nozzle.” (Rankin et al., 2017, p. 138)

### 3: [[Rotating Detonation Gas Turbine]]
**RDE vs PDE in a Gas Turbine**:
RDE Advantages:
- High power density
	- Reduces engine size
	- Less surface area for heat transfer losses
- No valves
- Already annular flow
- **Lower Unsteady pressure magnitudes than a PDE**
RDE Drawbacks:
* High power density = high heat xfer
* Inlet design complex:
	* Minimize pressure losses
	* Isolate compressor from RDE waves
* High exhaust temperatures
	* Need for dilution
* Unsteady turbine inlet conditions

**T63 Experiment**
[[Reverse-Flow Gas Turbine]] like the M250:
- No modification to turbomachinery
- Open-Loop integration configuration
- Ejector style dilution system
- #idea: can we use unsteady blowing or get clever with the dilution injection to damp pressure fluctations?
- ![[Pasted image 20251016181434.png]]
- **Pressure fluctuations almost completely eliminated in the HPT:** see [[RDC Unsteady Pressure Damping via Turbomachinery]]
- ![[Pasted image 20251016181630.png]]
- [[RDC Unsteady Pressure]]:
	- ~15-20% fluctuations
- Turbine efficiency:
	- Difficult to measure accurately for an RDC due to high variations in pressure and temperature (inherent unsteadiness). They say they got non-physical values from standard component efficiency calculations. See the discussion in [[Rotating Detonation Gas Turbine]] and the rationale for using "[[Turbine Factor]]" instead of isentropic efficiency:
- Results:
- ![[Pasted image 20251016195715.png]]
- ![[Pasted image 20251016195607.png]]
 - **Turbine showed no damage after ~20 minutes of testing!**
 - These are very awesome, this shows a **clear almost 5 point improvement** to the turbine factor when using the RDC!
	 - Disclaimers:
		 - Assumed perfect conversion of fuel energy
			 - If the OEM combustor was 15% better in combustion efficiency, then the power factor of the OEM turbine would be better.
		 - They didn't account for the stabilization bleed which could explain the discrepancy at higher energy inputs, but this was built into the vertical bars of the uncertainty.
		 - Heat loss from radiation/convection not considered, but expected to be minimal.
# Conclusions
- 1) The chemiluminesence (or in general just ways to see the detonation) is important for future rdc research, especially because it lets you compare 2D CFD to RDE experiments
- 2) Cool guidelines on RDC chamber design: “specific thrust, specific impulse, and static pressure distribution have been measured for a range of fuel injection schemes, air injection areas, detonation channel areas, aerospike plug nozzles, and converging/diverging nozzles.” (Rankin et al., 2017, p. 141)
- 3) For H2-Air and Ethylene-Air, the RDE spec impulses compare well to PDEs\theoretical calculations
- 4) it is possible to obtain similar stagnation pressure to thrust conversion efficiencies for hydrogen- and ethylene-fueled RDEs, which is important for future application and the desired operation of RDEs on heavier hydrocarbon fuels - idk really what that means tbh
- 5) Nozzles should be choked - and aerospikes are great for rdcs
- 6) RDE + Turbine is promising, 20 mins w/ no damage and similar to or better turbine factor was observed

Future work needed:
- Need to figure out the effects of the following on detonation:
	- Partial premixing
	- Lateral Relief (???)
		- Partial confinement something something
	- [[Detonation Wall Curvature]]
	- Turbulence
- One of the most important issues: [[Rotating Detonation Injectors]]
	- Optimize mixing
	- Minimize acoustic ineractions between plenums/combustor
	- reduce pressure loss so you can actually see the pressure gain
- Need to crack liquid hydrocarbons to be practical for propulsion.
- 

# The Op-Ed
- The turbine integration is the most promising thing ive seen on the subject, I like the discussion on using turbine factor instead of component efficiency due to the unsteadiness. And its very promising that it was comparable/better with an unoptimized turbomachinery.
- They also summarized and presented some good empirical data related to [[RDC Chamber Design]] and how it affects important performance parameters
- The importance of choking the outlet is given, the backpressure really makes a difference on the operation of the combustor.
- I think it would be very important to see if these findings hold up for other fuels, in particular hydrocarbons like methane, natural gas, and especially liquid fuels (as indicated in the conclusion/next steps section.)

# Follow-Ups
- General reviews on recent RDE work (1-3) #to_read_medium 
- Experimental/Computational studies on Fuel/Oxidizer compositions 4-6 #to_read_medium 
- Stagnation and Backpressure effects 7-10 #to_read_medium 
- Injection geometries 11-13 #to_read_medium 
- Channel Geometries 14-17 #to_read_medium 
- Curvature 18-20
- Exhaust Nozzles 21-24
- Exhaust static pressures & thrust 5,25 #to_read_high 
- Thermodynamic models based on ZND theory: 31,32 #to_read_medium 
-[[Schwer2013_Fluiddynamicsrotating]] 6
- **Effect of size on RDC performance 16 #to_read_high** 
- **Curvature on detonation stability limit! 18 #to_read_high** 
- 

# Reference
[@Rankin2017_OverviewPerformanceApplication]
