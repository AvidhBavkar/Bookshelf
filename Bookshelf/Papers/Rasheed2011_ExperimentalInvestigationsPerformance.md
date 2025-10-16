status:: to_read  
# Summary
An off-the-shelf 1000HP turbine is put downstream of a can-annular 8 tube pulsed-detonator. The uncertainty in turbine efficiency is high (+-10%) but no measurable impact was observed. The overall efficiency of the rig (combustor + turbine) is suggested to increase by ~4%
***** 

# Metadata:
Title: Experimental Investigations of the Performance of a Multitube Pulse Detonation Turbine System
Authors: [[Adam Rasheed]], [[Anthony H. Furman]], [[Anthony J. Dean]]
Year: 2011
CiteKey: Rasheed2011_ExperimentalInvestigationsPerformance
Zotero_Link: zotero://select/items/@Rasheed2011_ExperimentalInvestigationsPerformance
URL: https://arc.aiaa.org/doi/10.2514/1.B34013
### Tags:

#PGC 
[[Pressure Gain Combustion]]

# Abstract
A multitube [[Pulse Detonation Combustor]] consisting of eight unvalved tubes arranged in a can-annular configuration was integrated with a single-stage [[Axial Turbine]] nominally rated for 10 lbm=s, 25,000 rpm and 1000 hp. The multitube [[Pulse Detonation Combustor - Turbine]] hybrid was operated using [[Ethylene-Air]] mixtures for runs of 5 min to achieve thermal steady state in order to quantify performance at two operating conditions using simultaneous and sequential firing patterns. Analysis of these data reveal that turbine efficiency under pulse detonation-combustor-fired operation was indistinguishable from steady performance within the 8 points measurement uncertainty. Furthermore, the pulse-detonation-combustor-turbine hybrid system demonstrated a potential 25% improvement in efficiency once corrections were made for the suboptimal fueling design, which resulted in lower-than-anticipated combustion efficiency. The present work is promising as it suggests that a pulse detonation-combustor-turbine hybrid engine performance benefit can be realized with further development.

# Goal/Question
Quantifying the turbine performance and overall efficiency of a [[Pulse Detonation Combustor - Turbine]] gas-turbine like system.

# Methodology
- Hardware:
	- ![[Pasted image 20251014194438.png]]
	- [[Multitube PDC]]
		- 8 **unvalved** tubes
			- Air is continuously flowing
				- Unchoked relative to the primary plenum.
			- Fuel is pulsed injection via high-speed valves
		- [[Can-Annular]] Configuration
			* [[Coaxial Cooling Liner]] used to cool w/ "secondary air":
				- Eventually dumped to merge w/ main stream as dilution air 
	- 
		- 30 Hz (per tube)
		- Water-Cooled [[Spiral DDT geometry]] used to help assist detonation
	- Single-Stage [[Axial Turbine]]
		- Nominally rated for 10lbm, 25,000 RPM, **1000 hp**
		- From a "locomotive turbocharger"
			- Not optimized or designed for unsteady forcing
		- Compressor served as air-brake [[Compressor Air-Brake Dyno]].
	- ![[Pasted image 20251014194458.png]]
- Instrumentation:
	- Mass-flows, static/total pressures and temperatures
	- [[Optical Pyrometer]]
	- Accelerometers
	- [[Strain Gages]] for rotordynamics
	- [[Blade Tip Timing]] ( I think)
	- [[Piezo-electric Pressure Sensor]]
		- PCB 113A
		- Only used for a short fires (too hot in steady state)
	- Thermocouples - at the turbine mid-span.
	- To measure [[Detonation Wave Velocity]]:
		- 2 [[Ion Probe]] used for wave speed measurements
- Test condition:
	- Condition A: 75 kW , 12000 RPM
	- Condition B: 150 kW, 15600 RPM
- 
# Results
- Achieved [[Detonation Wave Velocity]] equal to CJ Speed. Maybe this is easier in a PDE?
- A good point brought up: "While the component turbine efficiency might be lower, what really matters is the overall cycle efficiency change" (paraphrased)
- 3 modes compared:
	- 1: Steady Cold Flow
	- 2: Steady Heated Flow (from a vitiator) - kind of analagous to a "normal" combustor
	- 3: "Fired" PDE Active at 20hz (per tube)
- **There was a malfunction in the cooling system, 1/8 of the PDEs is inactive!** They think this is the reason why the turbine efficiency is lower in the PDE cases due to non-axisymmetric flow/cold-spot.
- ![[Pasted image 20251015194634.png]]
- The grey hatched region is the overall uncertainty band, and the smaller bars at the 95% confidence interval.. huge uncertainty
- Qualitative discussion on [[PDE Firing Pattern]]:
	- The sequential firing sounded "choppy" and the pressure measurements showed high misfiring, potentially caused by hot gas from one tube pre-igniting the next one.
	- The "all at once" pattern was qualitatively smoother but they kept blowing up the burst disk, obviously indicating huge pressure pulses.
- Considering the "overall efficiency" of the combustor + turbine:
- ![[Pasted image 20251015195032.png]]
- Note: Not the cycle/thermodynamic efficiency! Just the rig (combustor + turbine) - compressor is referring to the [[Compressor Air-Brake Dyno]]
- ![[Pasted image 20251015195139.png]]
- **At one op-point, it looks like the PDE shows a higher efficiency than the steady-burner case, almost 5%!**
# Conclusions
* "No measurable adverse impact to turbine efficiency"
	* yes but the uncertainty is +- 10%..
* "Potential 4 point improvement to rig efficiency"
* Encouraging results - since nothing here is optimized for PDC operation.
* Future improvements:
	* Add valves so its not unvalved
	* Better fuel-injection system
	* Just put the turbine directly behind the tubes, no plenum no stator
	* Design a turbine specifically for PDC flows
		* "Most challenging"
		* Such a turbine might look completely different from existing turbine designs, and might require a completely new paradigm.
		* Since the current option is an off-the-shelf turbine, there was no way it was gonna be better anyway.
	* 

# The Op-Ed
- Very high uncertainty, the claim that its no worse and maybe a little better is kind of strange when you **have a 20% wide band on turbine efficiency lmao**
	- largely due to the location where they were installed (some where directly behind the "cans" and others were in between). To get the uncertainty they literally just took the average and looked at how far the readings were from the average, kind of crude (see Figure 6).
- Interesting discussion on several techniques to determine the turbine inlet temperature using:
	- Thermocouples
	- Turbine Outlet Temperature
	- Emissions, O2, and CO2
	- Phi, corrected w/ emissions data for UHC.
- Good derivation of how a [[Compressor Air-Brake Dyno]] works, uploaded derivation there.
- [[Emissions Probe]] system
	- "Sample probes used today are not designed to ingest the PDC exit flows. For these reasons, characterizing the emissions directly downstream at the exit of a PDC is very difficult."
- **Overall, a promising paper:** The uncertainty was high so I'm not convinced its a *good* idea, but it looks like its not *not* a bad idea to put a turbine downstream of a PDC. Especially considering that nothing here is optimized for PDC integration, its pretty cool that the efficiency doesn't take a massive hit at least!

# Follow-Ups
- Engine System Performance of Pulse Detonation Concepts using the NPSS Program - **28** #to_read_high
- 19-21 Liquid Detonation Papers  #to_read_medium
- Thermal Efficiency 20% improvement in ground power settings 29,30 #to_read_high 
	- “potential improvements in thermal efficiency of almost 20% compared with conventional gas-turbine technology 29,30” (Rasheed et al., 2011, p. 586)
- PDC Turbine from:
	- Japan [31] #to_read_medium 
	- China [32] #to_read_medium 
- Prev experimental studies:
	- Hoke [33] #to_read_medium 
	- Schauer [34] #to_read_medium 
	- Both above is an auto turbocharger (130kRPM) behind a PDC
	- Dean [35] - steam turbine blasted with a PDC. #to_read_medium 
	- [36-38] Stoich C2H4-O2 PDE at Steady state #to_read_medium
	- [39] "novel optical technique using a laser pointer and a photodiode to characterize the pulse-to-pulse change in turbine rpm"
	- 
# Reference
[@Rasheed2011_ExperimentalInvestigationsPerformance]
