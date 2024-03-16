# Lineup's Formula3HP Headphone Amplifier
###### Warning: always beware of high sound volume, it can damage your hearing! First close your volume control and slowly increase the volume

![enclosure](https://github.com/Wanderingidea/Formula3HP/assets/42114791/5beeb39b-3402-41bb-8f09-ad7a01f713b2)

This headphone amplifier built from discrete components was designed by ***Lineup***, a forum member of diyaudio.com. I slightly modified it.

It is very easy to build, beginner friendly I think, simple, uses cheap components, Class-A, tolerant, and sounds unbelievably good. "Smooth", "impressed", "nice clarity and detail", "Vocals are clear and bass is good" are a few comments from diyaudio.com. Without exaggeration I fully endorse these. This is a high quality headphone amplifier!
I use it almost every day since I built it in July 2021. That proves this is a robust design.

## Schematics
The schematics for one channel: 
![schematics](https://github.com/Wanderingidea/Formula3HP-headphone-amplifier/assets/42114791/15b8bff8-806b-4180-9ffd-d1eeb49d375c)

A stereo logaritmic potmeter of 20K is used as the volume control. I advise to use ALPS, they are more expensive but definitely worth it. It prevents vague problems.
RL are the headphones, 32 ohm or higher. I use Beyerdynamics DT770 Pro 80 ohm headphones.

The voltage amplification is 4x.

Q1 and Q2 can be replaced with BC547(C) and BC557(C) respectively. For Q3 originally a BD139 transistor was used. Like said the circuit is pretty tolerant of using different components. I mostly used leftover components without problems.

Q3 becomes a bit hot so this transistor should be mounted on a small heatsink. R1, R6 and R7 also heat up. Use 3 to 5 Watt type resistors for these.

Being such a simple circuit a piece of perfboard is used, one for each channel. 

I used an old 12V switched power supply without any problems. The amplifier is free of hum and noise.

## Simulated measurements
Attached are the LTSpice simulation files for FFT and frequency measurements.<br>
The following simulation graphs largely speak for themselves:
### Frequency/Phase:
![freq](https://github.com/Wanderingidea/Formula3HP/assets/42114791/43f02a09-f3db-453b-9d8e-f08a0f296780)
### FFT:
![FFT](https://github.com/Wanderingidea/Formula3HP/assets/42114791/637edfbb-658a-42c2-b7b2-b46d2fbb8c42)

Numbers resulting from a FFT simulation:
```
Direct Newton iteration for .op point succeeded.
N-Period=100
Fourier components of V(out)
DC component:-0.00360058

Harmonic	Frequency	 Fourier 	Normalized	 Phase  	Normalized
 Number 	  [Hz]   	Component	 Component	[degree]	Phase [deg]
    1   	1.000e+03	1.995e+00	1.000e+00	    0.30°	    0.00°
    2   	2.000e+03	1.222e-05	6.124e-06	   73.88°	   73.58°
    3   	3.000e+03	6.213e-06	3.114e-06	   36.19°	   35.89°
    4   	4.000e+03	1.025e-05	5.138e-06	  171.41°	  171.11°
    5   	5.000e+03	8.069e-06	4.045e-06	 -178.13°	 -178.44°
    6   	6.000e+03	6.439e-06	3.228e-06	 -179.48°	 -179.78°
    7   	7.000e+03	5.525e-06	2.769e-06	  179.75°	  179.45°
    8   	8.000e+03	4.844e-06	2.428e-06	  179.97°	  179.67°
    9   	9.000e+03	4.307e-06	2.159e-06	 -179.97°	 -180.28°
   10   	1.000e+04	3.876e-06	1.943e-06	  179.98°	  179.68°
Total Harmonic Distortion: 0.001106%(0.235859%)

pout_rms: RMS(v(out)*i(rl))=0.0304637 FROM 0 TO 0.1
ppsu: AVG(abs(v(v+)*i(v1)))=1.14035 FROM 0 TO 0.1
```
## PCB
Scribble how to place the components on the perfboard: 
![scribble](https://github.com/Wanderingidea/Formula3HP/assets/42114791/5a5c339a-fe4b-4e24-bd31-a37b7794f928)

## Constructing
The two mono boards are 'sandwiched' to be able to fit in the small enclosure: 
![pcb](https://github.com/Wanderingidea/Formula3HP/assets/42114791/8a6837b6-ebe9-4da0-9689-86c483e44a45)
![pcb2](https://github.com/Wanderingidea/Formula3HP/assets/42114791/6548a4c5-0585-4d5e-86b8-742266c1ebeb)
![pcb3](https://github.com/Wanderingidea/Formula3HP/assets/42114791/71e4d850-029b-4991-9651-d391bc8b6636)
![pcb4](https://github.com/Wanderingidea/Formula3HP/assets/42114791/5289aecf-3c63-41d9-85e3-2e30e4fbf31b)

Being a class-A amplifier it heats up a bit, but not too much. However a ventilated enclosure is recommended.<br>
An old piece of perfboard is used as a template to drill the ventilation holes. Use a light oil or WD40 as lubrication for the drill and take your time: 
![drill template ventilation holes](https://github.com/Wanderingidea/Formula3HP/assets/42114791/c4ce4b41-0632-4a68-8967-893af275f838)

After drilling all holes I brushed the aluminium. Do not use sandpaper for this but use Scotch Brite or similar, lubricated with WD40.
![holes drilled, brushed case](https://github.com/Wanderingidea/Formula3HP/assets/42114791/6e6b1db1-52f8-41b8-8e02-fa7d927ed0c7)
![continue1](https://github.com/Wanderingidea/Formula3HP/assets/42114791/953c6fad-ca6c-472d-bb7d-f89165cf6d80)

I stripped an old cat-5 network cable to use the internal cables for audio.<br>
All ground cabling is connected at the back of the enclosure soldered to a screw. It is not necessary to isolate the input, output and power input from ground. 
![continue2](https://github.com/Wanderingidea/Formula3HP/assets/42114791/75f9b5a0-d77a-4d9c-9012-36b252244a13)

Finished
![finished](https://github.com/Wanderingidea/Formula3HP/assets/42114791/6aca888e-5836-42b1-97b1-27ef55015564)
<sub>the small knob is for balance control which I later removed</sub>

## Troubleshooting
If you hear strange whistles or other weird noises coming out of the headphones but the amplifier is working, chances are the amplifier is oscillating.
The following options may solve that problem:
- try an other powersupply
- put a lowpass filter directly before the volume potmeter:
a resistor of 2.2k in series, a capacitor of 330p to ground
- put one 'clamp on´ ferrite bead around the left/right audio output wires

If you hear a hum check the ground wires going to one point close to the input of the amplifier.
