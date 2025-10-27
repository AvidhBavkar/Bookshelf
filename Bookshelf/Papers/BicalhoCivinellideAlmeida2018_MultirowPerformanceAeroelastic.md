
# Summary
 *Numerical study of an Axial HPC w/ unsteady backpressure (RDC). Unsteady forcing and propagation from stage-to-stage is found to get worse at low frequencies, and be somewhat negligible above the BPF.*
******

# Metadata:
Title: Multirow Performance and Aeroelastic Analyses of a [[Compressor]] Subjected to Disturbances from [[Pressure Gain Combustion]]
Authors: [[Victor Bicalho Civinelli de Almeida]], [[Dieter Peitsch]]
Year: 2018
CiteKey: BicalhoCivinellideAlmeida2018_MultirowPerformanceAeroelastic
Zotero_Link: zotero://select/items/@BicalhoCivinellideAlmeida2018_MultirowPerformanceAeroelastic
URL: 

### Tags/Topic
#Aeroelasticity #PGC #Numerical
[[Aerodamping]]

# Abstract
Aiming at radical increase of gas turbine thermal efficiency, novel [[Pressure Gain Combustion]] (PGC) processes are being investigated. These inherently unsteady techniques include pulse/rotating detonation, shockless explosion and wave rotor combustion. They all introduce periodic disturbances on the flow dynamics, which strongly challenge performance and aeroelastic design. The current work appraises to which degree this additional unsteadiness affects an industrial high pressure compressor (HPC). Single and multirow unsteady computational fluid dynamics and aeroelastic analyses characterize how the induced disturbances travel through the system, driving a departure from the steady state design. Assessments with one to four rows (two stages) delineate how farther upstream the disturbance dynamics must be considered by the performance and aeroelastic designers. To that end, unsteady damping as well as maximum stresses are evaluated. The nonlinear harmonic balance method is employed to determine the aerodynamic work and corresponding damping. Modal forcing from unsteady time-resolved runs is then projected into the blade surface. The structural response is obtained through harmonic response analyses, in a decoupled fluid-structure interaction (FSI) fashion.

# My Notes
- Numerical Investigation
- Axial HPC subjected to unsteady static backpressure
	- Backpressure is a simple sine wave:
	- ![[Pasted image 20251013090926.png]]
	- Not really sure how accurate that is compared to a real RDC pressure trace
- 3 configurations tested:
	- Single Rotor (R6)
	- Rotor-Stator (R6-S6)
	- 2 stage Rotor-Stator (R6-S6-R7-S7)
- Little bit of confusion about the following:
	- "pitch ratio right downstream of rotor 6 (i.e., between R6-S6) is always kept unitary, so to proper model the upstream-propagating disturbances without phasing error related to rotor-stator interfacing methods."
	- What does the pitch-ratio (pitch:chord) being 1 have to do with phasing-error?
	- For the multi-stage setup, they use a technique called [[Profile Scaling]] to minimize computational time, more details in ref 20.
- Side note: [[Blisks]] are more subject to aeroelastic concerns than non-blisks (duh) and you can find more blisks in modern engines, especially in the high-pressure compressor/turbine stages.
- Good discussion on [[Unsteady Damping]]:
	- Unsteady damping is defined as this (epsilon):
	- **NOTE: In this compressor experiment, unsteadiness travels upstream from 2 to 1!!**
		![[Pasted image 20251013092712.png]]
	- where phi is some state variable (commonly static/total pressure)
	- As you can see, unsteady damping is **defined across 2 stations**, 1 and 2. That's like the "amount of damping across a component"
		- Damping of 0 means that the unsteadiness (delta phi) is totally the same across the stage (delta phi 2 = delta phi 1)
		- Doing some algebra:
			$$\Delta \Phi_1= \Delta \Phi_2(1-\epsilon_{2,1})$$
		- Recalling that disturbances travel UPSTREAM, from 2 to 1, if the damping is 1, then there is no unsteadiness upstream regardless of however much unsteadiness is there downstream.
	- We can then also do more math (not shown) to consider the cumulative damping (across n stages):
		- If you assume all stages have the same unsteady damping, the cumulative damping is this:
			![[Pasted image 20251013094141.png]]
		- When you plot that:
		-![[Pasted image 20251013094235.png]]
		This is a cool plot, it tells you for instance:
		If you're unsteady damping is 75% per stage, by 3 stages you've damped out 98% of the unsteadiness.
		But if your unsteady damping is -26% per stage, by 3 stages you've doubled the unsteadiness.
		
		More rigourously, you can take the partial derivative wrt n to see how sensitive unsteady propogation is to unsteady damping for a particular stage. Obv. smaller stage counts are more sensitive:
		![[Pasted image 20251013094851.png]]
		
Back to the CFD Results:
For rotor alone:
![[Pasted image 20251013095627.png]]
Findings:
**Lower Frequency Disturbances are much higher loss (0.125 BPF vs 1)**
- For frequencies near or above the BPF, no real pressure loss observed.
	- Explanation:
		- When the high-pressure wave comes by, the flow seperates off the TE suction side
		- When the low-frequency wave comes by, the flow gets "sucked" and the incidence is negative, temporarily choking the compressor.
		- Alternately, the pressure pulses drive mass-flow swings, which is like swinging up and down along a characteristic of a compressor map.
Here's the damping results:
![[Pasted image 20251013100215.png]]
Conclusion from this study: Rotor alone is not capable of "chopping up" the disturbance wave at low frequencies.

**Study 2: Rotor/Stator**
Plot of efficiency vs frequency:
![[Pasted image 20251013100550.png]]
Again: low-frequency bad.
	- Particularly at 0.25BPF, the flow starts to reattach just as the next wave starts and fucks it up again.
	- At 0.125, theres a bit of time where the flow can reattach before the next wave comes along.
![[Pasted image 20251013100843.png]]
**Study 3: Rotor-Stator-Rotor-Stator**
- At BPF above 0.5, there's virtually no effect on the R6 (upstream) rotor from the pressure fluctations.
- But at low frequencies below 0.125, the disturbances are amplified.
![[Pasted image 20251013101219.png]]

#### Structural Results
- [[Mode Superposition Harmonic Analysis]] employed:
	- "Harmonic Analysis" - frequency response
	- "Mode superposition" - instead of solving the full system, solver first finds the natural modes. Then combining these modes to response is approximated. I don't really know how yet.
- "to match the disturbance pattern, the minimum global damping for zero [[Nodal Diameter]] was used"
- I'm not sure I fully follow whats going on, but it looks like they took the unsteady forcing from the unsteady CFD results and applied it to a CSM/FEA model, what they found was this:
- ![[Pasted image 20251014143109.png]]
- When the excitation frequency was less than the BPF, the stresses were massive, up to 250x the steady-state case!

# Goal/Question:
What happens to an HPC compressor when subjected to unsteady backpressure (like from an [[Rotating Detonation]] Combustor?)

# Methodology:
- [[Numerical Study]].
- Axial HPC subjected to unsteady static backpressure
	- Backpressure is a simple sine wave:
	- ![[Pasted image 20251013090926.png]]
	- Not really sure how accurate that is compared to a real RDC pressure trace
- 3 configurations tested:
	- Single Rotor (R6)
	- Rotor-Stator (R6-S6)
	- 2 stage Rotor-Stator (R6-S6-R7-S7)
# Claims/Conclusions:
1) The number of rows to simulate in this type of work is **strongly dependent on the wave amplitude.**
	1) *"For weak enough waves (here with roughly Ad < 10% of outlet pressure) detectable but not serious depreciation in efficiency and stability was encountered. However, for larger amplitudes (such as Ad = 20 %), a decrease as high as 25 % was observed. In summary, the **upstream-traveling pressure waves from PGC might not be a performance show-stopper, as long as the amplitudes are kept within reasonable limits.** This may be achieved by a proper unsteady combustion scheduling design, an effective plenum geometry etc."*
2) Unsteady damping (shown above) is a good descriptor of unsteady flow in axial turbomachines.
	1) *"It represents quantitatively whether a wave is attenuated of amplified along its path, and to each degree. Although it was used to assess temperature and pressure, any other periodically varying state variable might be investigated. Additionally, the unsteady damping cumulative formulation (Eqs. (3) and Eqs. (4)) sheds light into how much local unsteady damping should be expected from each station of a multirow/stage turbomachinery component to achieve a global attenuation. Its validity was checked in a two-stage disturbed setup"*
3) At low frequencies (0.125 BPF), this design showed **negative unsteady damping** (aka amplification)
4) CSM/FEA results show meaningful increase in displacement/stress in presence of disturbances, **particularly at low EO excitation**
# The Op-Ed
- Great paper, very useful read.
- Excellent discussion on [[Unsteady Damping]], a good parameter that can be employed to understand how unsteadiness propagates through stages.
- Seems to indicate that if your **RDC operates above the BPF of the compressor, you see negligible propogation of unsteadiness**
- **Low frequency oscillations are especially bad for turbomachinery**
- But modeling the pressure pulse of an RDC as a pure sinusoidal profile seems to not really be super representative, it should probably be more impulsive.
- 

# Follow-Ups
- [[Decouple FSI Approach]] (Page 2)
- [[Nonlinear Harmonic Balance]] - 16
- 11: Pressure measurements & Attenuation in a Pulse Det Turbine system **- 1!**
- [[Hysteretic Damping]] Page 8 ref 25, 26 - 2!

# Reference
[@BicalhoCivinellideAlmeida2018_MultirowPerformanceAeroelastic]
