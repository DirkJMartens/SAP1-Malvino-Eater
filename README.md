# SAP1-Malvino-Eater
Wire wrapped implementation of Albert Malvino's SAP1 computer, similar to Ben Eater's "8 bit CPU". 

Like thousands of others, I watched Ben Eater's YouTube series on how to "Build an 8-bit CPU from scratch". 
This video series uses the SAP-1 (Simple As Possible 1) computer as described in "Digital Computer Electronics" 
by Albert Malvino and Jerald Brown. 

And like thousands of others, I wanted to build my own. With a few differences: 
  - Use wire-wrapping instead of breadboards because I wanted it to be longer-lasting. 
  - Stay closer to Malvino's original design for the SAP-1. 
  - Added a dual 7-segment display to visualize the W-bus content in HEX-format. 
  - Add some blinkenlights to visualize:
    - LED bar graphs for Accu, B-register, Output-register, Instruction register 
    - LEDs for the control signals (La, Ea, Lb, Eb, Ep, CE ...) and the Program Counter 
    - the ring counter indicating the stage of the Fetch/Execute cycle 
    - the instruction decoder 
In short, I wanted it much more of a visual CPU. 

Done using mostly 74LS-series ICs and installed on a 20cmx30cm (8"x12") PCB. 

Most important specs: 
  - 4 bits address bus with 16 bytes RAM memory
  - 8 bits data bus
  - 4 instructions: Add, Sub, Out, Load
  - Clock signal can be single stepped, or auto-run with variable clock speed (up to a few dozen Hz)
