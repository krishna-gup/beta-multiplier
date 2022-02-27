# Design of a Beta Multiplier Current Reference Circuit in 28nm CMOS Technology

# Table of Contents

- [Abstract](https://github.com/krishna-gup/beta-multiplier/blob/main/README.md/#Abstract)
- [Tools Used](https://github.com/krishna-gup/beta-multiplier/blob/main/README.md#tools-used)
- [Working](https://github.com/krishna-gup/beta-multiplier/blob/main/README.md/#Working)
- [Reference Circuit and Output](https://github.com/krishna-gup/beta-multiplier/blob/main/README.md#reference-circuit)
- [Implementation](https://github.com/krishna-gup/beta-multiplier/blob/main/README.md#implemented-circuit-schematic)
- [Simulation](https://github.com/krishna-gup/beta-multiplier/blob/main/README.md#dc-analysis-parameters)
- [Conclusion](https://github.com/krishna-gup/beta-multiplier/blob/main/README.md#conclusion)
- [Author](https://github.com/krishna-gup/beta-multiplier/blob/main/README.md#author)
- [Acknowledgements](https://github.com/krishna-gup/beta-multiplier/blob/main/README.md#acknowledgements)
- [References](https://github.com/krishna-gup/beta-multiplier/blob/main/README.md#references)

# Abstract

In this paper, I am going to design a current reference circuit using 28nm CMOS Technology. Current Reference circuits are widely used in both analog and digital designs to bias the transistor in the required region of operation.
The current reference needs to have a high output resistance to mimic an ideal current source and low output voltage. Along with the basic requirements, the output reference current must not vary with subtle changes in temperature, voltage, and process. 
This complete design and implementation would be on VLSI Technology, which thereby ensures low power, low cost, and small size.

# Tools Used

- Synopsys Custom Compiler: The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.
- Synopsys Prime Wave: PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.
- Synopsys 28nm PDK: The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# Working

Beta Multiplier is a type of current reference circuit that produces a PTAT (Proportional to Absolute Temperature) current which ensures the maintenance of a constant gm (Transconductance) across PVT Variations. The transistors are biased into the saturation region.

The beta-multiplier should be self-biased to achieve independence from the supply voltage, which means that the reference current must be derived from its output and vice versa. This is done by bootstrapping the current in either of the two branches of the beta-multiplier to each other using a combination of NMOS and PMOS current mirrors.

# Reference Circuit

![beta_mul](https://user-images.githubusercontent.com/83169108/155857516-c427ae23-de97-4723-b504-7c65060fea08.jpg)

# Reference Output Waveform

![op](https://user-images.githubusercontent.com/83169108/155858085-f5cd85ed-ca19-4a39-a2bb-381ed9c975e2.jpg)

# Implemented Circuit Schematic

![sch](https://user-images.githubusercontent.com/83169108/155883470-52169baf-0160-4db0-ba28-1e50a2a2aae7.jpg)

# Designed Symbol

<img width="254" alt="Screenshot (274)" src="https://user-images.githubusercontent.com/83169108/155883637-a31e2342-6034-4042-a678-9035f4343347.png">

# Test Bench Schematic

<img width="489" alt="Screenshot (275)" src="https://user-images.githubusercontent.com/83169108/155883681-6368a406-ed9c-40c9-b2f5-6a3546ea53f6.png">

# DC Analysis Parameters

<img width="254" alt="Screenshot (268)" src="https://user-images.githubusercontent.com/83169108/155883538-f8de3494-8fdc-4025-a2e0-bbb9295d5230.png">

# Simulated Output Waveforms

<img width="345" alt="Screenshot (270)" src="https://user-images.githubusercontent.com/83169108/155883590-55ad99f1-7d5d-4ebe-b45c-e5db3b8da9c2.png">

# Conclusion

The referenced circuit of a Beta Multiplier, viz, a PVT Invarient Current Source has been simulated and designed successfully, and the reference waveform and the actual waveform obtained from Primewave matches. The given current reference circuit is invarient of changes in Process, Supply Voltage or Temperature variations, and produces a PTAT (Propotional to Absolute Temperature) Current.

# Author

Krishna Gupta, Jaypee Institute of Information Technology, Sector 62, Noida

# Acknowledgements

- Kunal Ghosh, Co-Founder, VSD Corporation Pvt. Ltd. 
- Analog IC Design Hackathon, Hosted by Indian Institute of Technology, Hyderabad
- Synopsys India
- Chinmay Panda, IIT-H

# References

- M. Lee and K. Moez, “A 0.5-1.5V Highly Efficient and PVT-Invariant Constant Transconductance Reference in CMOS,” IEEE Transactions on Circuits and Systems I: Regular Papers, 2020
- B. Razavi, Design of analog CMOS integrated circuits. Tata McGraw-Hill Education, 2002
- Matti Paavola, et. Al, A Micropower Voltage, Current, and Temperature Reference for a Low Power Capacitive Sensor Interface. Helsinki University of Technology, Espoo, Finland, 2007
- Soumyajit Mandal, et. Al, Fast Startup CMOS Current References. MIT CA, 2006
- Shailesh Singh Chouhan, Kari Halonen. A 0.67-μW 177-ppm/◦C All-MOS Current Reference circuit in a 0.18µm CMOS Technology. IEEE-2016
