# iiitb_rtc-Real Time Clock

### Introduction
This is a real time clock, an integrated circuit, provides time to the microcontroller.It consists of oscillatory circuit, counter, register. Oscillatory circuit made of quartz crystal generates clock signal with high level of stability. Prescaler also called as frequency divider scales the clock producing a clock of frequency 1Hz. Counter using generated 1Hz clock signal counts the seconds and apparently minutes, hours. The time values are stored in a register. Real-time circuit is interfaced with microcontroller by Advanced Peripheral Bus following Advanced Microcontroller Bus Architecture (AMBA) bus protocol there by communicating time with microcontroller.  Real-time clock provides accurate time track to the device so all the events take place at the right time. This system functions reliably with optimum CPU and memory space usage.

### Block diagram

![rtcbd](https://user-images.githubusercontent.com/62790565/184196172-5bb0eee9-9785-4821-b242-71568a29f803.PNG)

### RTL Simulation
#### Installation of Icarus Verilog (iVerilog) and GTKwave on ubuntu
Open terminal and type the following commands to install iverilog and GTKwave.
```
$ sudo add-apt-repository ppa:team-electronics/ppa 
$ sudo apt-get update 
$ sudo apt-get install iverilog gtkwave
```

#### To clone the repository,simulate the results, Enter the following commands in your terminal :
```
$ git clone https://github.com/Bandaanusha/iiitb_rtc
$ cd iiitb_rtc
$ iverilog -o iiitb_rtc_out.out iiitb_rtc.v  iiitb_rtc_tb.v
$ vvp iiitb_rtc_out.out
$ iverilog iiitb_rtc.v  iiitb_rtc_tb.v
$ gtkwave iiitb_rtc_out.vcd
```

#### Simulation Waveforms
![iiitb_rtc_output_waveform](https://user-images.githubusercontent.com/62790565/181303117-9da92814-20e7-4b28-b0ac-55b03bb8a11e.PNG)

### Synthesis
Synthesis transforms the simple RTL design into a gate-level netlist with all the constraints as specified by the designer. In simple language, Synthesis is a process that converts the abstract form of design to a properly implemented chip in terms of logic gates. Yosys is a framework for Verilog RTL synthesis.

#### Installation of yosys on Ubuntu
Open the terminal and type the following commands to install yosys
```
$ sudo apt-get install build-essential clang bison flex \ libreadline-dev gawk tcl-dev libffi-dev git \ graphviz xdot pkg-config python3 libboost-system-dev \ libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make
$ sudo make install
```

#### To synthesize the design, Enter the following commands in your terminal
```
```

### Gate Level Simulation
GLS is generating the simulation output by running test bench with netlist file generated from synthesis as design under test. Netlist is logically same as RTL code, therefore, same test bench can be used for it.

#### To Simulate results, Enter the following commands in your terminal
```
```

### Simulation Waveforms
Pre - synthesis simulation waveform: 
Post - synthesis simulation waveform:

## Contributors
- Banda Anusha
- Kunal Ghosh
- 
## Acknowledgements
- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd.
- Dantu Nandini Devi, Postgraduate Student, International Institute of Information Technology, Bangalore.
- 
## Contact Information
- Banda Anusha, Postgraduate Student, International Institute of Information Technology, Bangalore Banda.Anusha@iiitb.ac.in
- Dantu Nandini Devi, Postgraduate Student, International Institute of Information Technology, Bangalore nandini.dantu@gmail.com
- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd. kunalghosh@gmail.com

## References
- Real-Time Clocks (RTCC) ,Microchip technology,  https://www.microchip.com/en-us/products/clock-and-timing/components/real-time-clocks.
- RTC Verilog Code - Elecdude, www.elecdude.com.

