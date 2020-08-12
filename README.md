# SAR_Logic

This project is on SAR Logic IP designing using an open-source tool. The design includes Flow/FreePDKs provided by VLSI Computer Architecture Research Group (VLSIARCH) at Oklahoma State University (OSU). 

Table of contents
=================
<!--ts-->
   

   * [ A Glance SAR Logic Circuitry](#A-Glance-SAR-Logic-Circuitry)
   * [Block Diagram of the SAR Logic](#Block-Diagram-of-the-SAR-Logic)
   * [Circuit Diagram of 4 bits SAR logic](#Circuit-Diagram-of-4-bits-SAR-logic)
   * [Tool to view and simulate SAR logic IP](#Tool-to-view-and-simulate-SAR-logic-IP)
        * [ngSpice](#ngSpice) 
        * [Installing Ngspice in Ubuntu 18.04](#Installing-Ngspice-in-Ubuntu-18.04)
        * [Running the Simulation](#Running-the-Simulation)
        * [Pre-Layout Simulation](#Pre-Layout-Simulation)
   * [Pre-Layout Performance Characteristics](#Pre-Layout-Performance-Characteristics)
        * [input voltage and Comparator output waveforms](#input-voltage-and-Comparator-output-waveforms) 
        * [start of conversion and end of coversion bit  waveforms](#start-of-conversion-and-end-of-coversion-bit-waveforms) 
        * [Data output bit D9 and D8  waveforms](#Data-output-bit-D9-and-D8-waveforms)
        * [Data output bit D7 and D6  waveforms](#Data-output-bit-D7-and-D6-waveforms)
        * [Data output bit D5 and D4  waveforms](#Data-output-bit-D5-and-D4-waveforms) 
        * [Data output bit D3 and D2  waveforms](#Data-output-bit-D3-and-D2-waveforms)
        * [Data output bit D1 and D0  waveforms](#Data-output-bit-D1-and-D0-waveforms)     
   * [Future Work](#future-work) 
<!--te-->

## A Glance SAR Logic Circuitry
To obtain the basic information on analog to digital converter: tap the link [this](/basic/intro.pdf).
To learn more about SAR Logic models and its working principle: tap this link [this](/Basic/SARtypes).
To view the implementation and specification: tap this link [this](/Basic/working).

## Block Diagram of the SAR Logic

 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/block_diag.png">
</p>


## Circuit Diagram of 4 bits SAR logic


 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/ckt_diag.jpeg">
</p>



## Tool to view and simulate SAR logic IP
 

### Ngspice

It is a open source spice simulator of electric and electronic circuits. 

### Installing Ngspice in Ubuntu 18.04

 Open the terminal and type the following commands to install Ngspice
```
$  sudo apt-get install ngspice
```
### Running the Simulation


To enter the Ngspice Shell, open the terminal & and move to the directory containing the netlist you want to simulate.
Type the following commands:
```
$ ngspice

ngspice 1 ->  source <filename>.cir
```

To exit from the Ngspice Shell type:
```
ngspice 1 ->  exit
```

### Pre-Layout Simulation

To clone the Repository and download the Netlist files for Simulation, enter the following commands in your terminal.

```
$  sudo apt install -y git
$  git clone https://github.com/shalini161/SAR_Logic
$  cd SAR_Logic/ngSpice_simulation/
$  ngspice sar.cir

```



## Pre-Layout Performance Characteristics

###  input voltage and Comparator output waveforms



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/clk_comp.png">
</p>



###  start of conversion and end of coversion bit  waveforms



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/reset_eoc.png">
</p>



###  Data output bit D9 and D8  waveforms



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/D9_8.png">
</p>



###  Data output bit D7 and D6  waveforms



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/D7_6.png">
</p>



###  Data output bit D5 and D4  waveforms



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/D5_4.png">
</p>



###  Data output bit D3 and D2  waveforms



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/D3_2.png">
</p>



###  Data output bit D1 and D0  waveforms



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/D1_0.png">
</p>


## Future Work

1. 



## Contributors 

- **Shalini Priya** 
- **Kunal Ghosh** 
- **Philipp Gühring** 



## Acknowledgments


- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd.
- Philipp Gühring, Software Architect, LibreSilicon Assocation



## Contact Information

- - Shalini Priya, M.Tech Embedded System, NIT Jamshedpur priyashalini161@gmail.com
- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd. kunalghosh@gmail.com
- Philipp Gühring, Software Architect, LibreSilicon Assocation pg@futureware.at

