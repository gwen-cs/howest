# Computer Architectures lab 4.2

### Electronics
#### OHM's law
1. To connect a LED on the 5v there is a resistor needed, calculate the minimum resistor value and connect the red LED. *Note: the LED has a max value of 20mA and a forward voltage of 2V.*
>   150 Ω
2. Calculate this for the blue LED that has a max value of 20mA and a forward voltage of 3,4V.
>   80 Ω
3. To connect a LED on the 3.3v there is also a resistor needed, calculate the minimum resistor value and connect the red LED. *Note: the LED has a max value of 20mA and a forward voltage of 2V.*
>   65 Ω    
4. Calculate this for the blue LED that has a max value of 20mA and a forward voltage of 3,4V.
>   0 (led brand niet !! )

#### Circuits - breadboard
5. Draw the circuits for Q1 - Q4
> ( zie bijlage )
6.  What happens if there is a higher resistor between the 5V and the LED?
> indien te hoog heeft de let niet genoeg om te kunnen branden. of geeft minder licht
7.  Draw the schematic icon of a pushbutton
>   ( zie bijlage )
8. How does a pushbutton work?
>   ja kan de kring sluiten met de button 
9. Draw the electronic schematic and the breadboard schematic with a pushbutton, the LED and resistor stays the same.
>    ( zie bijlage )
### Fast charging
10. Calculate the time it takes to fully charge your phone.
> Wh=(mAh×3.7V)÷1000 ==> Wh=(3279×3.7)÷1000=12.13Wh ==> 12.13÷0.85=14.27Wh  ==> 14.27÷20=0.7135uur  ==> 0.7135×60=42.8minuten
11. With a battery drain of 1W how long does it take before the battery of your phone is empty?
> Tijd= 12.13 / 1 = 12.13uur

#### And functions

12. Draw the following circuit (electronic and breadboard), when 2 push buttons return true the LED will turn on.
> (zie bijlage )
13. Explain the working of this circuit
> A EN B moeten gesloten zijn om de lamp te laten branden.
14. Draw the truth table for this circuit

> A false   B false     = false 
---
> A false   B true      = false 
---
> A true    B false     = false
---
> A true    B true      = true

15. Calculate the needed resistor
> 150 Ω

16. Add a 3th button and second led. Both LED's are on when all push buttons return true. Recalculate the needed resistor.
> 75 Ω

#### OR functions

17. Draw the following circuit (electronic and breadboard), when 1 of the 2 push buttons return true the LED will turn on.
> (zie bijlage )
18. Explain the working of this circuit
> A OF B moeten gesloten zijn om de lamp te laten branden.
19.  Draw the truth table for this circuit
> A false   B false     = false
---
> A false   B true      = true
---
> A true    B false     = true
---
> A true    B true      = true

20. Calculate the needed resistor
> 150 Ω

#### Circuits

21. Create a parallel circuit with 4 LED's. There are 2 ways to do this, with in each node a resistor or with 1 resistor in series with the parallel circuit. Draw for both possibilities the electrical and breadboard circuit.
> (zie bijlage )
22. Calculate the resistor values (for 4 resistors and for 1 resistor in series)
> 150 Ω of ( 4 x 37.5 Ω )

23.  Create a circuit with 2 AND functions and 1 OR function, where the last AND get's the input of the OR function and the first AND function. In this circuit add 3 LED's.
Draw the schematics with the logic gates, electronic and breadboard.
> (zie bijlage )

24.    What possible combinations of button presses will the LEDs light up? Calculate this using DNV. This can be done via the truth tables or faster using the logic laws.
> A false   B false      C  false       = false
---
> A false   B false      C  true        = false
---
> A false   B true       C  false       = false
---
> A false   B true       C  true        = true
---
> A true    B false      C  false       = false
---
> A true    B false      C  true        = true
---
> A true    B true       C  false       = false
---
> A true    B true       C  true        = true
---

#### Shift register
25. Draw a circuit with the shift resistor and 8 LED's
> (zie bijlage )

26. What binary value has to be send to the shift resistor to turn LED 2, 4, 5 and 8 on?
> 0 1 0 1 1 0 0 1
> 
> Einde (test git)