# ALU8bit
A simple project to program an 8bit adder using the MOJO FPGA, written in Lucid. Of note is that it actually performs the operation via bitshifting, instead of using the inbuilt functions that were in the language. Mainly because I didn't know they were there at the time.
## Starting up (Prerequisites)
Preferably Utilise:<br>
Mojo IDE: https://alchitry.com/pages/mojo-ide <br>
Xillinx's ISE Design Suite for Windows 10 - 14.7  - https://www.xilinx.com/support/download/index.html/content/xilinx/en/downloadNav/design-tools.html <br>
### Tools
Embedded Micro MOJO V3 - https://alchitry.com/collections/all/products/mojo-v3 <br>
Embedded Micro IO Shield - https://alchitry.com/collections/all/products/io-shield <br>
### Format
* adder.luc -> Does addition using bits provided.<br>
* alumod.luc -> Controls which operation occurs.<br>
* bitshift.luc -> aids in choosing which bitshift module will be used. Coordinates the next 3 modules.<br>
* bitshiftleft.luc -> Bitshift Left<br>
* bitshiftright.luc -> Bitshift Right<br>
* bitshiftrightwithsign.luc -> Bitshift right with sign<br>
* boolean.luc -> Performs a boolean operation on the 2 sets of 8 bits provided, and displays the result in the third LED array.<br>
* comparator.luc -> Utilised in the bitshift right with sign, to tell if we should light up the <br>
* io_shield.ucf -> Config file for IO_shield. leave well alone.<br>
* mojo_top.luc -> Overall controller. Really just acts as a pointer into alumod.luc<br>
* multiplier.luc -> Performs multiplication.<br>
* totaladder.luc -> Spawns 8 copies of adder.luc, for all 8 bits.<br>
