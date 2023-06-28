# Lineup's Formula3HP Headphone Amplifier
![enclosure](https://github.com/Wanderingidea/Formula3HP/assets/42114791/b32013b2-bbdf-4d67-b492-3d04a94cd83f)

This headphone amplifier built from discrete components is a big step forward from a Cmoy like headphone amplifier. It was designed by ***Lineup***, a forum member of diyaudio.com. I slightly changed it.

It is very easy to build, beginner friendly I think, simple, uses cheap components, Class-A, tolerant, and sounds fantastic. My first impression is the power and impact it has, without raising the volume.
"Smooth", "impressed", "nice clarity and detail", "Vocals are clear and bass is good" are a few comments. Without exaggeration I fully endorse these.
I use it almost every day since I made it in July 2021. That proves this is a robust design.

## Schematics
The schematics for one channel: 
![schematics](https://github.com/Wanderingidea/Formula3HP/assets/42114791/65f5c9c0-e7a2-48b0-9922-2b63acd67aeb)

A stereo logaritmic potmeter of 10K-50K can be used as the volume control. RL are the headphones, 32 ohm or higher. I use Beyerdynamics DT770 Pro 80 ohm headphones.

Q1 and Q2 can be replaced with BC547 and BC557 respectively. For Q3 originally a BD139 transistor was used. Like said the circuit is pretty tolerant of using different components. I mostly used leftover components without problems.

Q3 becomes a bit hot so this transistor should be mounted on a small heatsink. R1, R6 and R7 also heat up. Use 3 to 5 Watt type resistors for these.
R1 consists of two resistors in series, 33 ohm each.

Being such a simple circuit a piece of perfboard is used, one for each channel. 

I used an old 12V switched power supply without any problems. The amplifier is free of hum and noise.

## Simulated measurements
Attached are the LTSpice simulation files for FFT and frequency measurements.<br>
The following simulation graphs largely speak for themselves:
![freq](https://github.com/Wanderingidea/Formula3HP/assets/42114791/d846f060-2235-43ff-8285-8f24ddabe9b1)
![FFT](https://github.com/Wanderingidea/Formula3HP/assets/42114791/8869eeff-0b2d-4410-b776-b5d830df68fe)

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
![scribble](https://github.com/Wanderingidea/Formula3HP/assets/42114791/686955b2-00e0-478d-bd84-819655fadfc6)

## Constructing
The two mono boards are 'sandwiched' to be able to fit in the small enclosure: 
![pcb](https://github.com/Wanderingidea/Formula3HP/assets/42114791/1b2ba66b-7da3-4893-a40a-7efcb419cb2d)
![pcb2](https://github.com/Wanderingidea/Formula3HP/assets/42114791/80e815ee-e60c-4fdc-81f8-d1de0a170d27)
![pcb3](https://github.com/Wanderingidea/Formula3HP/assets/42114791/02e514fb-9108-4528-9636-f4b992dd2b5e)
![pcb4](https://github.com/Wanderingidea/Formula3HP/assets/42114791/c7687410-4a56-4196-9204-9ddd41ca83a1)
![PCB III](https://github.com/Wanderingidea/Formula3HP/assets/42114791/f95fc15f-fec3-4d1b-9151-618dc412b291)

Being a class-A amplifier it heats up a bit, but not too much. However a ventilated enclosure is recommended.<br>
An old piece of perfboard is used as a template to drill the ventilation holes. Use a light oil or WD40 as lubrication for the drill and take your time: 
![drill template ventilation holes](https://github.com/Wanderingidea/Formula3HP/assets/42114791/f5bde9fb-ae85-4198-98ce-5ff7408a41aa)
After drilling all holes I brushed the aluminium. Do not use sandpaper for this but use Scotch Brite or similar, lubricated with WD40.
![holes drilled, brushed case](https://github.com/Wanderingidea/Formula3HP/assets/42114791/22c1dd03-1e66-4f07-a598-7398deee0fc3)
![continue1](https://github.com/Wanderingidea/Formula3HP/assets/42114791/5d19626c-91e3-41de-9f99-5133ec7447cf)
I stripped an old cat-5 network cable to use the internal cables for audio.<br>
All ground cabling is connected at the back of the enclosure soldered to a screw. It is not necessary to isolate the input and output from ground. 
![continue2](https://github.com/Wanderingidea/Formula3HP/assets/42114791/f13c28b0-7867-4b94-aac4-e926e6b4dd44)
Finished
![finished](https://github.com/Wanderingidea/Formula3HP/assets/42114791/f9ce640e-6cea-4e4c-9fc3-52ee081452ac)

## Troubleshooting
If you hear strange whistles and other noises coming out of the headphones but the amplifier is working, chances are the amplifier is oscillating.
The following options may solve the problem:
- try an other powersupply
- put a lowpass filter directly before the volume potmeter:
a resistor of 2.2k in series, a capacitor of 330p to ground
- check the ground going to one point close to the input of the amplifier
