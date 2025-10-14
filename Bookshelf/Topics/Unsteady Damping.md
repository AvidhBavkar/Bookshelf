Good discussion/explainer on Unsteady damping from [[BicalhoCivinellideAlmeida2018_MultirowPerformanceAeroelastic]]:

## Discussion/Explanation from Bicalho et al.
Good discussion/explainer from [[BicalhoCivinellideAlmeida2018_MultirowPerformanceAeroelastic]]

Unsteady damping is defined as this (epsilon):
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