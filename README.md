# Tremolo pedal

## About
A Tremolo effect pedal, which modulates the guitar signal's amplitude by a generated triangular wave with adjustable frequency. The modulation frequency range is from about 0.5Hz to 10Hz. The circuit has the following stages:

1. Input: guitar signal reception by a P10 (6.35mm) Jack;
2. Oscillator: using a NE555, a square symmetrycal wave is generated, and converted to a triangular wave (with the frequency adjustable by a potentiometer). The wave then passes through a Op Amp buffer;
3. Amplification: The guitar signal is amplified by a ratio of about 2.5 with no distortion/clipping. This is needed because there is power loss at the modulation stage;
4. Modulation: After the amplification, the guitar signal goes through a variable resistor (representing the 'Depth' of the effect) in series with a LDR (Light Dependent Resistor), illuminated by a Led supplied by the oscillator (see the schematic, might get confusing). When the generated wave (from -2V to +2V) is > 0, the LED lights up and the LDR reduces its resistance greatly (from about 2M to about 50k on the best scenario), and the output is the tension divided by these 2 resistors. Since the LDR resistance never reaches zero, there is power loss. Hence, the amplification stage is required. It's basically a voltage divider, with the grounded resistance being the LDR (varying from 2M to 50k), and the 'supply' resistance being the Depth level.
5. Output: modulated signal goes to a P10 Jack.

## Schematic
*These are only the oscillator and modulation circuits, without the inputs, outputs and supply circuits. Please open the Eagle project for the full circuit.*

Oscillator:

![Oscillator schematic](https://github.com/felipeb-oliveira/Tremolo-pedal/blob/master/images/oscillator.PNG)

Modulation:

![Modulation schematic](https://github.com/felipeb-oliveira/Tremolo-pedal/blob/master/images/modulation.PNG)

## Board
![Board](https://github.com/felipeb-oliveira/Tremolo-pedal/blob/master/images/board.PNG)


