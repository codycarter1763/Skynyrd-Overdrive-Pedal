# Skynyrd Overdrive Pedal

# About
The Skynyrd overdrive pedal is my attempt at bringing that sought-after southern rock Peavey Mace sound that Skynyrd used into any setup. Having drawn inspiration from tube screamers, my goal was to create a highly versatile pedal that can be used as a clean boost, solid drive into another drive pedal, or a standalone pedal that will add new tonal possibilites to your arsenal. 

# About Lynyrd Skynyrd and the Peavey Mace
Back when Lynyrd Skynyrd first got started, guitarists Gary Rossington and Allen Collins used Marshall Super Lead Plexis for hits such as Sweet Home Alabama and Free Bird. Though, due to Skynyrd blowing Marshall amps from repeated usage at high volumes during touring, they opted for a more reliable amp. There comes Peavey and the Peavey Mace amp, known for it's high headroom, volume, and reliability. 

![peavey_mace_amp](https://github.com/user-attachments/assets/cdf0adc1-f726-4c4b-94d4-13b51018eee5)

# Parts List

# Circuit Diagrams and Analysis
This is the current circuit diagram for the pedal. As I update any component values through my own experimentation I will update it here. 

## TS-808 Schematic
This is a circuit diagram for the famous TS-808 Ibanez Tube Screamer that I based my design off of. Known for it's versatile and signature sound, it is the perfect platform to see what makes a great pedal work.

For the JFET switch, this was implemented to keep the costs of units down instead of using a 3 DPDT true bypass switch. The JFET switch is not needed and is easily removable, take a look at my schematic later on.
![image](https://github.com/user-attachments/assets/6ce63595-d519-4455-b223-f8c443c194db)

Fun fact, if you wanted to turn your TS-808 into a higher gain pedal like the TS-9, all you do is switch out the 100 ohm resistor for a 470 ohm, and the 10kOhm to 100kOhm for higher gain. Such a mod can even be implemented into a double-pole switch for added versatility.
</br>
![image](https://github.com/user-attachments/assets/248e7cc1-4c83-41ba-835d-968f6a55969b)

## Peavey Mace Tone Stack
This is a snapshot for part of the normal channel for the Peavey Mace. In amps, the tone stack is what sets the EQ and how the amp will mostly sound. It will get you right in the ballpark to the signature amp sound. For the normal channel, it had only a treble and bass control.  
</br>
![Screenshot 2025-06-23 154348](https://github.com/user-attachments/assets/b7872640-5427-4c80-8586-dc0dd1abeed3)

## How It Fits Together
In the tube screamer schematic, I dropped the Mace tone stack in between the first and second amp stage, and set the tube screamer tone control to a fixed value. For added versatility, I switched C5 from 270pF to 330pF for more bass and added 500k pots for more range of EQ. 
![image](https://github.com/user-attachments/assets/e495e16a-2838-42f7-b5f3-220cb3c18c65)

## Design Choices and Other Aspects To Skynyrd's Sound
Now that the tone stack was installed, the pedal worked on the first try and right off the bat was very close to the Peavey Mace. Though, there was still some room for improvement since the pedal sounded too clean and did not have that Marshall/Mace fuzz to the low end. 

### Input Buffer Stage
This stage takes the high impedance guitar signal and steps it down to a lower impedance to prevent tone sucking. For this stage, I switched out the stock 2SC1815 NPN with a BC549 since that is what I had on hand. 

Zin = R1 + (R2//β*R3) = 1k + (510k // 250*(10k)) = 424kOhms

Ie = 
re = 25mV / Ie
Zout = (re + (R1 / β)) / (1 + β) = 
![image](https://github.com/user-attachments/assets/eeb68f74-6847-4997-83e0-d68ea38d9191)


# Circuit Board and Design

# Closing
