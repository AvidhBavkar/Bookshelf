# Summary

*****
# Metadata:
Title: Experimental Investigation of Mode Shape Sensitivity of an Oscillating Low-Pressure Turbine Cascade at Design and Off-Design Conditions
Authors: Damian M. Vogt, Torsten H. Fransson
Year: 2007
CiteKey: Vogt2007_ExperimentalInvestigationMode
Zotero_Link: zotero://select/items/@Vogt2007_ExperimentalInvestigationMode
URL: https://asmedigitalcollection.asme.org/gasturbinespower/article/129/2/530/477705/Experimental-Investigation-of-Mode-Shape
### Tags:


# Abstract
The effect of negative incidence operation on mode shape sensitivity of an oscillating low-pressure turbine rotor blade row has been studied experimentally. An annular sector cascade has been employed in which the middle blade has been made oscillating in controlled three-dimensional rigid-body modes. Unsteady blade surface pressure data were acquired at midspan on the oscillating blade and two pairs of nonoscillating neighbor blades and reduced to aeroelastic stability data. The test program covered variations in reduced frequency, flow velocity, and inflow incidence; at each operating point, a set of three orthogonal modes was tested such as to allow for generation of stability plots by mode recombination. At nominal incidence, it has been found that increasing reduced frequency has a stabilizing effect on all modes. The analysis of mode shape sensitivity yielded that the most stable modes are of bending type with axial to chordwise character, whereas high sensitivity has been found for torsion-dominated modes. Negative incidence operation caused the flow to separate on the fore pressure side. This separation was found to have a destabilizing effect on bending modes of chordwise character, whereas an increase in stability could be noted for bending modes of edgewise character. Variations of stability parameter with inflow incidence have hereby found being largely linear within the range of conditions tested. For torsion-dominated modes, the influence on aeroelastic stability was close to neutral.

# Background/Notes:
Commonly, flutter in turbomachine blade rows is described by a [[Travelling Wave Mode Approach]] assuming that all the blades are oscillating in the same mode and at the same amplitude and frequency (seperated by phase).
- Reference 9: this is the **least stable condition** and thus overconservative.
If you consider **a linear superimposition** of contributions from all the blades, you get the [[Influence Coefficient Approach]]:
![[Pasted image 20251021100206.png]]
Here:
- The LHS is the unsteady pressure coeff. (called the "complex pressure coefficient) at any point (x,y,z) on blade m.
- This is saying that its a linear superposition of the complex pressure coefficients of all the other blades (n), multiplied by some phase shift $\sigma$ 
In simple words:

"The **unsteady pressure** on a non-vibrating reference blade (m) when the whole row vibrates in a travelling-wave pattern is **the sum of the influence from each neighboring blade's** motion, each **shifted in phase** according to its position"

ChatGPT had a great summarization:
##### 🧩 Step 1. The equation itself

![[Pasted image 20251021100753.png]]

It looks scary, but it’s really just saying:

> “The unsteady pressure on a non-vibrating _reference_ blade (m) when the whole row vibrates in a traveling-wave pattern is the sum of the influences from each neighboring blade’s motion, each shifted in phase according to its position.”

---

##### 🔹 Step 2. Left-hand side — the **traveling-wave mode (TWM)**

![[Pasted image 20251021100807.png]]

- This is the **complex pressure coefficient** (unsteady part) _acting on blade m_
    
- The whole cascade is vibrating together in a **traveling-wave pattern** (the mode shape)
    
- The pattern is defined by the nodal diameter (σ), which controls the inter-blade phase angle (IBPA = 2πσ/N)
    

So this left side is what you would _actually measure_ on one blade during a traveling-wave vibration test or CFD simulation.

---

##### 🔹 Step 3. Right-hand side — the **influence-coefficient (IC)** domain

![[Pasted image 20251021100822.png]]

This is the **influence coefficient** — it describes:

> the unsteady pressure on the _reference blade (m)_ caused by the motion of blade _n_ only.*

So you can think of it as a “building block.”  
If you know how one moving blade affects the rest of the row,  
you can predict what happens when **all** blades move together with certain phase lags (a traveling wave).

Each influence coefficient is a _complex pressure field_ that depends on location (x,y,z).

---

##### 🔹 Step 4. The exponential term

![[Pasted image 20251021100834.png]]

This adds the **phase shift** for blade n according to the traveling wave.  
It basically tells you how far behind or ahead blade n’s motion is compared to blade 0.

So this is the mathematical way to “rotate” the phase of each blade’s contribution before adding them up.

---

##### 🔹 Step 5. The summation

![[Pasted image 20251021100850.png]]
means:

> “Add up the pressure effect from every blade in the row (all neighbors), each with its correct phase shift.”

That’s what makes it a **superposition** of influence coefficients to reconstruct a traveling-wave condition.

### Unsteady Pressure -> Unsteady Force -> Net Work.
Okay, so now we have the complex (unsteady) pressure coefficients, I can multiply them by the normal vector and small areas to get **unsteady force** on the blade:
![[Pasted image 20251021102020.png]]
In the 3 orthogonal directions (axial, circumferential, torsional). Then we can make a matrix like this:
![[Pasted image 20251021102100.png]]
which is the "Force Matrix" -
- First index of the subscript: mode **causing** the force
- Second index of the subscript: direction in which the force is acting.
- Diagonal Terms: Forces that act in the same direction as the motion
- Off-Diagonal: Coupling between motions (flap motion causes torsion, etc.)



# Goal/Question
- Investigating the unsteady aerodynamics during [[Flutter]] of a [[Low-Pressure Turbine Aeroelasticity]] rotor. 
- Incidence is controlled, allowing study of aeroelasticity at off-design conditions
- 

# Methodology
* LPT Blade:
	* Aspect Ratio of 2
	* Tip Clearance = 1% span
	* 
* [[Annular Sector Cascade]]
	* 7 free blades
* One driven blade:
	* Two RB Bending Modes
	* One Torsion Mode
* Incidence is controlled.
* 

# Results
-

# Conclusions
- 

# The Op-Ed
- 

# Follow-Ups
- [1 ] - "One of the most complete compilations of flutter tests has been given by 1 , including data from both compressor and turbine cascades of annular as well as linear shape and at two-dimensional 2D blade oscillation"
	- Compares travelling wave & influence coefficient approaches
	- Both approaches compare well at low amplitudes!
	- Backed up by 2-4
	- #to_read_high 
- (5) - Influence of varying spanwise bending amplitude - **highly nonlinear** 
- (6) - Looking at effect of seperation in an LP Turbine
	- Stabilizing character! for the investigated mode only
- "Spanning an orthogonal mode space" - what is an orthogonal mode space??
- (7,8)- Travelling wave stuff
- 9: Travelling wave is "overconservative" #to_read_high 
- 

# Reference
[@Vogt2007_ExperimentalInvestigationMode]
