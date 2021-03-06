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
        * [Input Clock Pulse and Comparator Output waveforms](#Input-Clock-and-Comparator-Output-waveforms) 
        * [Start Of Conversion and End Of Coversion bit  waveforms](#Start-Of-Conversion-and-End-Of-Coversion-bit-waveforms) 
        * [Data output bit D9 and D8  waveforms](#Data-output-bit-D9-and-D8-waveforms)
        * [Data output bit D7 and D6  waveforms](#Data-output-bit-D7-and-D6-waveforms)
        * [Data output bit D5 and D4  waveforms](#Data-output-bit-D5-and-D4-waveforms) 
        * [Data output bit D3 and D2  waveforms](#Data-output-bit-D3-and-D2-waveforms)
        * [Data output bit D1 and D0  waveforms](#Data-output-bit-D1-and-D0-waveforms)
        * [EOC and all Data Output (D9 to D0) waveforms for analysis](#EOC-and-all-Data-Output-(D9-to-D0)-waveforms-for-analysis)
   * [Future Work](#future-work) 
<!--te-->

## A Glance SAR Logic Circuitry
To obtain the basic information on analog to digital converter: tap the link [this](/basic/intro.pdf).


To know about ADC specification: tap this link [this](/basic/specifications.pdf).


Explanation on SAR control logic working principle:  It uses the binary searching algorithm. The whole circuit is divided into two parts namely the upper half works as shift registers and the lower half as code registres. The RESET also called as SOC i.e start of conversion is applied for the first clock cycle. It helps to reset all the D flip-flop before the starting of conversion. In the second clock cycle the lower leftmost MSB flip-flop i.e D9 is set which gives the binary code 1000000000. In the next clock cycle, D8 sets and it acts as a clock pulse for D9 which allows the D9 flip-flop to store input from the comparator. So if the comparator input is high we get the output as 1100000000 or else it's 0100000000 as your output. So the same sequence continues for the rest flip-flops. At the 11th clock cycle, EOC i.e end of conversion signal is generated, showing the end of conversion for a single hold sample.

## Block Diagram of the SAR Logic

 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/block_diag.png">
</p>


*Note - SAR Control Logic is completely a digital circuit so the applied digital voltage is 1.8V according to spec. sheet for 180nm tech node. All the data output bits voltages are 1.8V each.

## Circuit Diagram of 4 bits SAR logic


 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/ckt_diag.jpeg">
</p>

*Note -   The 10-bit SAR Logic won't be visible clearly in the allotted image size, so used 4-bit SAR Logic for visibility purpose.


 ## Tools needed to view and simulate SAR_Logic IP
 
  <img align="left" width="45" height="45" src="/image/prelayout_image/logo.png">

### 1. Ngspice

[Ngspice](http://ngspice.sourceforge.net/devel.html) is a open source spice simulator tool for electric and electronic circuits.

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

To clone the Repository and simulate the Netlist, enter the following commands in your terminal.

```
$  sudo apt install -y git
$  git clone https://github.com/shalini161/SAR_Logic
$  cd SAR_Logic/ngSpice_simulation/
$  ngspice sar.cir
```



## Pre-Layout Performance Characteristics

###  Input Clock Pulse and Comparator Output waveforms



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/img1.png">
</p>



###  Start Of Conversion and End Of Coversion bit  waveforms



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/img2.png">
</p>



###  Data output bit D9 and D8  waveforms



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/img3.png">
</p>



###  Data output bit D7 and D6  waveforms



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/img4.png">
</p>



###  Data output bit D5 and D4  waveforms



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/img5.png">
</p>



###  Data output bit D3 and D2  waveforms



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/img6.png">
</p>



###  Data output bit D1 and D0  waveforms



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/img7.png">
</p>

### EOC and all Data Output (D9 to D0) waveforms for analysis

  <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/D9_D0.png">
</p>



## Future Work


The SAR logic circuit requires a large number of transistors hence, lead to more power consumption. So to increase the performance of SAR logic 
Non-Redundant Successive Approximation Register architecture proposed
by Rossi, can be used as it lessen the number of D Flip Flops

 
 

## Contributors 

- **Shalini Priya** 
- **Kunal Ghosh** 
- **Philipp Gühring** 



## Acknowledgments


- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd.
- Philipp Gühring, Software Architect, LibreSilicon Assocation



## Contact Information

- Shalini Priya, M.Tech Embedded System, NIT Jamshedpur priyashalini161@gmail.com
- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd. kunalghosh@gmail.com
- Philipp Gühring, Software Architect, LibreSilicon Assocation pg@futureware.at

