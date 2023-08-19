# SAP1-Malvino-Eater
Wire wrapped implementation of Albert Malvino's SAP1 computer, similar to Ben Eater's "8 bit CPU". 

Like thousands of others, I watched Ben Eater's YouTube series on how to "Build an 8-bit CPU from scratch". 
This video series uses the SAP-1 (Simple As Possible 1) computer as described in "Digital Computer Electronics" 
by Albert Malvino and Jerald Brown. 
And like thousands, I wanted to build my own. With a few differences: 
  - Use wire-wrapping instead of breadboards because I wanted it to be longer-lasting. 
  - Stay closer to Malvino's original design for the SAP-1.
  - Extend it slightly using a dual 7-segment display to visualize the bus content.
  - Add some blinkenlights to visualize:
    - the control signals (La, Ea, Lb, Eb, Ep, CE ...) 
    - the ring counter indicating the stage of the Fetch/Execute cycle 
    - the instruction decoder (Add, Sub, Out, Load)

All done using mostly 74LS-series ICs and installed on a 20cmx30cm (8"x12") PCB. 
