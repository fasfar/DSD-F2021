# Hex Calculator with Modifications

The two directories, *hexcalc* and *hexcalc_1* contain the design sources and constraint files for lab 4 and the modified lab, respectively. In this lab, a FPGA board was programmed to perform addition and subtraction calculations, as well as suppress leading zeros as part of the modifications.

The primary program, *hexcalc* uses a finite state machine to determine whether the user is inputting the first operand, the operator, or the second operand. The program constantly updates the state of the board based on the last button to be pressed/released.

## Modified Components

The objective of the modifications in this lab was to implement subtraction functionality and suppress leading zeros on the four-digit calculator. The subtraction functionality was achieved by adding variables to represent the subtraction button and a boolean that indicates whether the addition or subtraction button was pressed. The leading zeros of the operands and resultant value were suppressed by editing the *leddec16/vhd* file. In this file, the `anode` parameter was changed to only turn on the relevant digits within the four-digit display, rather than having them all turn on constantly.