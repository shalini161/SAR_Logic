# SAR_Logic

This project is on SAR Logic IP designing using an open-source tool. The design includes Flow/FreePDKs provided by VLSI Computer Architecture Research Group (VLSIARCH) at Oklahoma State University (OSU). 

## A Glance SAR Logic Circuitry
To learn more about SAR Logic models and its working principle: tap this link [this](/Basic/Types).
To view the implementation and specification: tap this link [this](/Basic/working).

## Block Diagram of the SAR Logic



## Circuit Diagram of 4 bits SAR logic





## Tool to view and simulate SAR logic IP
 

### Ngspice

It is use for open source spice simulator of electric and electronic circuits. Ngspice is an open project, there is no closed group of developers.

### Installing Ngspice in Ubuntu 20.04

 Open the terminal and type the following to install Ngspice
```
$  sudo apt-get install ngspice
```
### Running the Simulation


To enter the Ngspice Shell, open the terminal & type:
```
$ ngspice
```
To simulate a netlist, type:
```
ngspice 1 ->  source <filename>.cir
```

You can exit from the Ngspice Shell by typing:
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

###  input voltage and Comparator output



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/Vin_Clk.png">
</p>



###  start of conversion and end of coversion bit



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/soc_eoc.png">
</p>



###  Data output bit D9 and D8



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/D9_8.png">
</p>



###  Data output bit D7 and D6



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/D7_6.png">
</p>



###  Data output bit D5 and D4



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/D5_4.png">
</p>



###  Data output bit D3 and D2



 <p align="center">
  <img width="800" height="500" src="/image/prelayout_image/D3_2.png">
</p>



###  Data output bit D1 and D0



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

