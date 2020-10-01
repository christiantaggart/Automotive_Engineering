# Engineering Concepts:

##### Math:
- To convert cc / min to lbs. / hr. - Divide by 10.5
- To convert lbs. / hr to gal. / hr. - Divide by 6
- To convert cc / min to gal. / hr. - Multiply by .015873

## Engineering terms:
[Material Properties 101](https://www.youtube.com/watch?v=BHZALtqAjeM)
- Tough: Absorbs energy without breaking
- Ductile: Deforms under pressure (opposite of brittle)
- Hardness: resistance to compressive force
- Density = mass/volume

## Cavitation explained 
[src][n1waterpump_link]
- *How does cavitation occur?*
    - Rapid changes in pressure
>A reduction in pressure will actually reduce the temperature at which the coolant will boil, resulting in evaporation.

>This is one of the reasons why cooling systems are pressurized.  Pressurized coolant will have a much higher boiling point than if it were at atmospheric pressure. 



## Fuel System
- Fuel Tank
- **Fuel Pump:** [guide][fuelpump_guide]
- Fuel Pulsator
- Fuel Pump Control Module
- Fuel Rail
- Fuel Pressure Regulator (FPR)
- Fuel Filter
- Fuel lines (E85 friendly)
- ECU
- Fuel Pressure
- System Voltage
- Fuel Surge Tanks

### Fuel Injectors
> An injector is a solenoid, and it needs off time to work correctly. We can not realistically ask it to be 100% open all the time, so we normally use 80% in a fuel injector calculator, to give the injector 20% off time. [src][fuelsys_link]

- [Wiki: Brake-Specific Fuel Consumption or BSFC](https://en.wikipedia.org/wiki/Brake-specific_fuel_consumption) aka How much fuel you are using per Horsepower per hour.

[link to calculator][fuelinjector_calc_link]
- **Formula:** Gasoline hp = ((Injector_Size_CC / 10.5)* Cylinders * Injector_Duty_Cycle) / (√(43.5 / Fuel_Pressure_Psi) * BSFC) 
- **Formula:** E85 hp = Gasoline hp / 1.3
- **Example:** hp = ( (440 / 10.5) * 6 * 0.8) / ( √(43.5/36) * 0.6)
    - Gasoline hp 304 = 201.14 / .66
    - E85 hp 234 = (201.14 / .66) / 1.3

```js 
let	REFERENCE_FUEL_PRESSURE = 43.5;

function calculateHP(){
		var cylinders = $('#cylinders').val(); // # Cylinder motor has
		var pressure = $('#pressure').val(); // Fuel Pressure (PSI)
		var bsfc = $('#bsfc option:selected').val(); //0.5 for N/A; 0.55 for S/C; 0.6 for Turbo
		var cycle = $('#cycle option:selected').val(); // Injector Duty Cycle
		var size = $('#size').val() / 10.5; //Injector size full flow value (size) in CC/Min 
		var fuel = $('#fuel option:selected').val(); 

		var hp =  (size * cylinders * cycle) / (Math.sqrt(REFERENCE_FUEL_PRESSURE / pressure) * bsfc);

		if(fuel == 'e85'){
			hp = hp * 10/13; // Same as dividing by 1.3 
		}

		if (isNaN(hp) && show_error) {alert('Could not calculate. Please check your numbers.');}
		else if (! isNaN(hp)) {
			hp = Math.round(hp);
			$('#hp').html(hp);
			hp = Math.round( hp * .85);
			$('#whp').html(hp);
		}
}
```

<!-- ____________________ Links ____________________ -->
<!-- cavitation info and also N1 Waterpump vs Standard -->
[n1waterpump_link]:https://www.boostfactory.ca/blogs/tech-tuesday/rb26-n1-water-pump-rumours-theories-and-lies-demystified

[fuelsys_link]:https://www.gtrusablog.com/2016/12/fuel-system-for-nissan-skyline-gt-r.html

[fuelpump_guide]:http://www.stealth316.com/2-fuelpumpguide.htm

[fuelinjector_calc_link]:https://fuelinjectorclinic.com/hp-calculator