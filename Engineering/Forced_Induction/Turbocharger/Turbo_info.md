# TurboCharger Info:

##### Contents:
- Turbo Terminology Demystified
  - Housing:
    - Compressor
    - Turbine
  - Compressor:
    - Inducer
    - Exducer
  - Turbine:
    - Inducer
    - Exducer
  - Manifold
  - Flanges
  - Waste Gate
  - [Trim](1)
  - A/R Ratio
- Compressor Map
- System Components:
  - Blow Off Valve
- Turbocharged System Architecture:
  - Twin-Turbo Setups:
    - Parallel
    - Sequential



**[Back to top](#table-of-contents)**

---


## Turbo Terminology Demystified:
- CHRA: Center Housing Rotating Assembly

![garrett numbered cutaway](https://www.turbobygarrett.com/turbobygarrett/sites/default/files/turboTech/TurboTech-Basic/cutaway.gif)

- 1.) Ball Bearings (support and control the rotating group)
- 2.) Oil Inlet
- 3.) Turbine Housing (collects exhaust gases from the engine and directs it to the turbine wheel
- 4.) Turbine Wheel (converts exhaust energy into shaft power to drive the compressor)
- 5.) Center Housing (supports the rotating group)
- 6.) Oil Outlet
- 7.) Compressor Housing (collects compressed air and directs it to the engine)
- 8.) Compressor Wheel (pumps air into the engine)
- 9.) Backplate (supports the compressor housing provides aero surface)
[source: garrett](https://www.turbobygarrett.com/turbobygarrett/basic)
---

![Garrett Wheel Diagram](https://www.turbobygarrett.com/turbobygarrett/sites/default/files/turboTech/TurboTech-Advanced/Garrett_rotating_group_enlarged.jpg)
### Turbine Wheel _(Exhaust / Hot Side)_
- Inducer:
  - Base Larger diameter
    - Converts Exhaust Pressure as rotational force to drive Compressor
- Exducer:
  - Smaller upper portion of blades
  - Expels used exhaust gasses out to downpipe

### Compressor Wheel _(Intake / Cold Side)_
- Inducer:
  - Smaller upper portion of blades
  - Ambient Air Intake
- Exducer:
  - Base larger diameter
    - Ambient Air then gets compressed inside of the front of the housing
    - Pushes air through to Intercooler

**[Back to top](#table-of-contents)**

---



### Trim
- Trim = (Inducer^2 / Exducer^2 * 100)


**[Back to top](#table-of-contents)**

---



### A/R
###### (stolen from garrett):
- A/R is a numerical rating assigned to radial flow housings in order to distinguish the relative volumetric flow capacity of the housing.
- A/R does have units of length (inches or cm) based on the "A" over "R" description.
  - One must be careful because the A/R values can only be compared within a single family of housings.
  - 0.86 A/R of a GT28R and a 0.85 A/R of a GT40 have very different flow capacities.
- The term A/R is derived from:

```js
Q = "volumetric flow rate"
A = "cross-sectional area of the volute at the tongue"
R = "radius to the dynamic center (The dynamic center locates that point which divides the scroll area such that half the flow passes above and half the flow passes below the dynamic center.)"
V = "tangential component of velocity"

Q = A * V "(where V = K (flow rate constant) / R)"

Q = A * K/R

Q = K * A/R
```

Since K is a constant then A/R defines the flow capacity of hsgs within the same family.

- Compressor A/R:
  - Compressor performance is largely insensitive to changes in A/R; Typically there are not A/R options available for compressor housings.
  - Larger A/R housings are used to optimize the performance for low boost applications
  - Smaller housings are used for high boost applications.
- Turbine A/R:
  - Turbine performance is greatly affected by changing the A/R of the housing.
  - Turbine A/R is used to adjust the flow capacity of the turbine.
  - **Smaller A/R** will increase the exhaust gas velocity into the turbine wheel, causing the wheel to spin faster at lower engine RPMs giving a quicker boost rise.
    - This will also tend to increase exhaust backpressure and reduce the max power at high RPM.
  - **Larger A/R** will lower exhaust gas velocity and delay boost rise, but the lower backpressure will give better high-RPM power.
    - When deciding between A/R options, be realistic with the intended vehicle use and use the A/R to bias the performance toward the desired powerband.

**TL:DR** Small A/R == Faster spool & Lower TopEnd

**[Back to top](#table-of-contents)**

---


### Waste Gate:
- High Level Breakdown
- Types:
  - Internal
  - External

**[Back to top](#table-of-contents)**

---


### Compressor Maps

- Pressure Ratio:
``` js
PR = "Pressure Ratio";
B = "Boost Pressure in psi";
AP = "Atmospheric Pressure";
// AP @ Sea Level (0ft altitude) = 14.7
PR = (B + AP) / AP;
```
- Mass Air Flow:

- To calculate Rotary double Engine displacement (cubic centimeter)
```js
// WHEN CALCULATING FOR ROTARY:
// 13B Rotary Engine === 1308cc
const RD = 1308*2; // Rotary displacement Results in 2616cc
let D = RD // Displacement
```














### [Turbo Charger Comparison:](http://www.turbobricks.com/resources.php?content=turbodata)

| Compressor  |    |   |  |Turbine	    |   | | comp avg|
| :---- | :--- |:--- |:--- |:---|:--- |:--- | :--|
| Name  | Trim	 | Inducer  (Minor Diameter) | Exducer (Major Diameter) | Exducer (Minor Diameter)| Inducer (Major Diameter) | Trim   | avg |
| TD04-09B | 50 | 1.365 | 1.93 | 1.55 | 1.86 | x | 1.6475 |
| TD04-13G | 62 | 1.58 | 2 | 1.625 | 1.812 | x | 1.79 |
| T3 | 35 | 1.396 | 2.367 | x | x | x | 1.8815 |
| TB02 | 22 | 1.56 | 1.989 | 1.517 | 1.833 | x | 1.9015 |
| TD04H-15C | x | 1.638 | 2.165 | 1.743 | 2.028 | x | 1.9015 |
| TD04-15G | 55 | 1.625 | 2.187 | 1.625 | 1.812 | x | 1.906 |
| TD04H-15G | 55 | 1.625 | 2.187 | 1.74 | 2.047 | x | 1.906 |
| Mk 4 CT-12 | x | 1.535 | 2.283 | 1.732 | 2.047 | x | 1.909 |
| T3 | 40 | 1.484 | 2.367 | x | x | x | 1.9255 |
| T3 | 45 | 1.595 | 2.367 | x | x | x | 1.981 |
| TD05H-14B | 55 | 1.695 | 2.285 | 1.93 | 2.2 | x | 1.99 |
| TD05-16G | x | 1.814 | 2.223 | 1.911 | 2.184 | x | 2.0185 |
| T3 | 50 | 1.674 | 2.367 | x | x | x | 2.0205 |
| TD05H-14G | 62 | 1.8 | 2.285 | 1.93 | 2.2 | x | 2.0425 |
| TD04-17G | 54 | 1.744 | 2.382 | 1.625 | 1.812 | x | 2.063 |
| T3 | 55 | 1.76 | 2.367 | x | x | x | 2.0635 |
| TD05H-16G | 60 | 1.83 | 2.365 | 1.93 | 2.2 | x | 2.0975 |
| TD04-18T | x | x | x | 1.625 | 1.812 | x | x |
| T3 | 60 | 1.83 | 2.367 | x | x | x | 2.0985 |
| GT2510 | 63 | 1.86 | 2.344 | 1.626 | 2.067 | 62 | 2.102 |
| GT2530 | 63 | 1.86 | 2.344 | 1.883 | 2.098 | 76 | 2.102 |
| T3 | Super 60 | 1.9 | 2.367 | x | x | x | 2.1335 |
| Mk 3 CT-26 | x | 1.811 | 2.559 | 2.047 | 2.677 | x | 2.185 |
| TD05H-16G | 50 | 1.892 | 2.68 | 1.93 | 2.2 | x | 2.286 |
| TD05H-18A | 50 | 1.9 | 2.68 | 1.93 | 2.2 | x | 2.29 |
| TD05-18G | x | 1.97 | 2.652 | 1.911 | 2.184 | x | 2.311 |
| T04B | S | 1.904 | 2.75 | x | x | x | 2.327 |
| TD05H-18G | 55 | 1.992 | 2.68 | 1.93 | 1.93 | x | 2.336 |
| GT2835 | 48 | 1.923 | 2.773 | 2.02 | 2.204 | 84 | 2.348 |
| TD06-20G | x | 2.051 | 2.652 | 2.149 | 2.535 | x | 2.3515 |
| TD05H-20G | 60 | 2.07 | 2.68 | 1.93 | 2.2 | x | 2.375 |
| GTRS | 52 | 1.997 | 2.773 | 1.833 | 2.098 | 76 | 2.385 |
| GT2835 | 52 | 1.997 | 2.773 | 2.02 | 2.204 | 84 | 2.385 |
| T04B | T 5/6 | 2.032 | 2.75 | x | x | x | 2.391 |
| GT35 | 52 | 2.016 | 2.795 | 2.453 | 2.677 | 84 | 2.4055 |
| T04E | 40 | 1.87 | 2.95 | x | x | x | 2.41 |
| GT2835 | 56 | 2.071 | 2.773 | 2.02 | 2.204 | 84 | 2.422 |
| GT2835R | 56 | 2.071 | 2.773 | 2.09 | 2.204 | 90 | 2.422 |
| T04B | Super S | 1.904 | 3 | x | x | x | 2.452 |
| T04B | V | 2.18 | 2.75 | x | x | x | 2.465 |
| T04E | 46 | 2.003 | 2.95 | x | x | x | 2.4765 |
| GT2540 | 46 | 2.016 | 2.972 | 1.833 | 2.098 | 76 | 2.494 |
| GT3037 | 48 | 2.059 | 2.972 | 2.145 | 2.34 | 84 | 2.5155 |
| T04B | H | 2.298 | 2.75 | x | x | x | 2.524 |
| GT3037 | 52 | 2.145 | 2.972 | 2.145 | 2.34 | 84 | 2.5585 |
| T04E | 54 | 2.17 | 2.95 | x | x | x | 2.56 |
| HKS T04E | 57 | 2.196 | 2.925 | 2.266 | 2.785 | 62 | 2.5605 |
| T04E | 50 | 2.122 | 3 | x | x | x | 2.561 |
| GT37 | 52 | 2.157 | 2.992 | 2.614 | 2.854 | 84 | 2.5745 |
| GT35 | x | 2.157 | 2.997 | 2.453 | 2.677 | 84 | 2.577 |
| T04B | Super V | 2.18 | 3 | x | x | x | 2.59 |
| T04E | 57 | 2.23 | 2.95 | x | x | x | 2.59 |
| GT3037 | 56 | 2.223 | 2.972 | 2.145 | 2.34 | 84 | 2.5975 |
| T04E | 60 | 2.29 | 2.95 | x | x | x | 2.62 |
| **HKS T04S** | 60 | 2.301 | 2.972 | 2.523 | 2.894 | 76 | 2.6365 |
| T04B | Super H | 2.298 | 3 | x | x | x | 2.649 |
| T04B | 60-1 | 2.324 | 3 | x | x | x | 2.662 |
| T04B | 62-1 | 2.441 | 3 | x | x | x | 2.7205 |
| GT3040 | 50 | 2.262 | 3.198 | 2.145 | 2.34 | 84 | 2.73 |
| GT40 | 50 | 2.283 | 3.228 | 2.591 | 3.031 | 73 | 2.7555 |
| GT3240 | 54 | 2.352 | 3.198 | 2.106 | 2.289 | 84 | 2.775 |
| GT37 | x | 2.327 | 3.228 | 2.614 | 2.854 | 84 | 2.7775 |
| TS04 (T-57) | x | 2.3 | 3.304 | x | x | x | 2.802 |
| **HKS T04R** | 63 | 2.601 | 3.276 | 2.523 | 2.894 | 76 | 2.9385 |
| T-61 | x | 2.382 | 3.544 | x | x | x | 2.963 |
| **HKS T04R/GT63** | GT63 | 2.626 | 3.307 | 2.547 | 2.921 | GT76 | 2.998 |
| GT40 | 54 | 2.547 | 3.465 | 2.547 | 3.031 | 84 | 3.006 |
| T-78 GREDDY | x | 2.598 | 3.543 | 2.559 | 2.913 | x | 3.0705 |
| T-88 GREDDY | 33D | 2.598 | 3.543 | 2.846 | 3.346 | x | 3.0705 |
| T-64 | x | 2.49 | 3.67 | x | x | x | 3.08 |
| T-66 | x | 2.58 | 3.584 | x | x | x | 3.082 |
| **HKS T51 KAI** | 56 | 2.742 | 3.666 | 2.785 | 3.198 | 76 | 3.204 |
| T-88 GREDDY | 34D | 2.744 | 3.74 | 2.846 | 3.346 | x | 3.242 |
| T-70 | x | 2.72 | 3.85 | x | x | x | 3.285 |
| T-72 | x | 2.84 | 4.03 | x | x | x | 3.435 |
| GT42 | 53 | 2.925 | 4.016 | 2.961 | 3.228 | 84 | 3.4705 |
| **HKS T51 SPL** | 56 | 2.984 | 3.986 | 2.785 | 3.198 | 76 | 3.485 |
| T-76 | x | 3.02 | 4.03 | x | x | x | 3.525 |















**[Back to top](#table-of-contents)**

---
[Trim](#trim)
**[Back to top](#table-of-contents)**































---
**[Back to top](#table-of-contents)**
