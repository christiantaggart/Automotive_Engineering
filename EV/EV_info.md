# Electric Race Car

Design & Engineering Resources:
- [Electric Equations ](http://simplemotor.com/calculations/)
- [PF & other helpful info about AC motor (3-Phase)](http://www.engineeringtoolbox.com/power-factor-electrical-motor-d_654.html)
- [How to Calc HP](http://www.wikihow.com/Calculate-Horsepower)
- [Volts - Watts - Amps: Conversions](http://www.renewableedge.com/calculate_volts_amps_watts.html)
- [Power & torque](http://www.epi-eng.com/piston_engine_technology/power_and_torque.htm)

---
Retail:
- [EVWest Motor (with info): $18,488.00](http://www.evwest.com/catalog/product_info.php?cPath=8&products_id=300&osCsid=p38692ag9dte5e2mcuv8fo07b4)
- [evsource](https://evsource.com/)

---

### HorsePower:
- Imperial HorsePower is equivalent to 745.7 watts.
  - Electrical motor ratting horsepower (HP) is equivalent to 746 watts.
- Metric horsepower is equivalent to 735.5 watts.
- One horsepower was deemed to be the equivalent of one horse lifting 33,000 pounds over one foot in one minute on the surface of the Earth.
See Link: [What is HorsePower]

### Conversions-to-HP (w/ Electrical Specs):
- **DC Horsepower 	(Volts x Amps x Efficiency)/746**
![](img/EV HORSEPOWER CALC_V=volt_i=AMP_EF=Efficientcy.jpg)
- **AC Horsepower 	(Volts x Amps x 1.732 x Eff x PF)/746**
- V = Volts (Voltage will be expressed in volts)
- I = Amps (Current will be expressed in amps)
- Eff = Efficiency (Efficiency will be expressed as a percentage.)
  - The motor should have these units of measurement written on it
- PF = [Power Factor]
  - It is common to define the Power Factor as the cosine of the phase angle between voltage and current - or the `cosφ`.



---
References:

[What IS HorsePower]: https://www.carwow.co.uk/guides/glossary/what-is-horsepower

[Power Factor]:http://www.engineeringtoolbox.com/power-factor-electrical-motor-d_654.html

---

### Email VIA Shawnie:

"EV propulsion calculations:

"Driving on hills
Higher voltage comes in handy when going up hills- a long drawn out hill (remember a 5% grade doubles power needed)  can easily
demand more than 3C for longer than the recommended time  from our 100 ah batteries-putting them in an area that may reduce their
lifespan and create heat in the cell.
If the vehicle is to be used in mountainous areas or for high performance use, larger ah batteries are needed because of this C factor. A
side benefit of course would be longer range- but a costlier pack."

Performance
Now we get to the fun part, calculating HP
V x A = watts,    and  watts/746 = HP      so  V x A / 746 = HP

If we had a 144 volt pack of 200ah batteries, and a 1000 amp controller, using the above formula we could have  193 HP, (at a 5C draw)  
and if we had 288 volt pack of 100ah batteries we could have potentially  386 HP ! (these are calculated without efficiency included,
figure about 85% efficient)  
Only one problem, that much electrical power put into the motor could easily destroy it rather quickly !  The common "in the field"
estimate of KW power a 9" motor can handle (for short periods) is 100 KW.  So using the above formulas, 144 volt system should be
limited to about 700 amps, and the 288 volt system to 350 amps. Still, 135 hp is pretty good for a small car.  NOTE: use high power levels
at your own risk for motor damage.

http://ev-propulsion.com/EV-calculations.html"
