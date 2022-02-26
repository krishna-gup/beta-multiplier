# Design of a Beta Multiplier Current Reference Circuit in 28nm CMOS Technology

# Table of Contents

# Abstract

In this paper, I am going to design a current reference circuit using 28nm CMOS Technology. Current Reference circuits are widely used in both analog and digital designs to bias the transistor in the required region of operation.
The current reference needs to have a high output resistance to mimic an ideal current source and low output voltage. Along with the basic requirements, the output reference current must not vary with subtle changes in temperature, voltage, and process. 
This complete design and implementation would be on VLSI Technology, which thereby ensures low power, low cost, and small size.

# Tools Used

- Synopsys Custom Compiler
- Synopsys Prime Wave 
- Synopsys 28nm PDK

# Working

Beta Multiplier is a type of current reference circuit that produces a PTAT (Proportional to Absolute Temperature) current which ensures the maintenance of a constant gm (Transconductance) across PVT Variations. The transistors are biased into the saturation region.

The beta-multiplier should be self-biased to achieve independence from the supply voltage, which means that the reference current must be derived from its output and vice versa. This is done by bootstrapping the current in either of the two branches of the beta-multiplier to each other using a combination of NMOS and PMOS current mirrors.

# Reference Circuit

![beta_mul](https://user-images.githubusercontent.com/83169108/155857516-c427ae23-de97-4723-b504-7c65060fea08.jpg)

# Reference Output Waveform

<img width="311" alt="ReferenceOP" src="https://user-images.githubusercontent.com/83169108/155857524-4e88703a-ddb0-4d6d-82ad-c94191d9e0b2.png">

# Implemented Circuit Schematic

# DC Analysis Parameters

# Simulated Output Waveforms

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
