# SAP1-Malvino-Eater
Wire wrapped implementation of Albert Malvino's SAP1 computer, similar to Ben Eater's "8 bit CPU". 

Like thousands of others, I watched Ben Eater's YouTube series on how to "Build an 8-bit CPU from scratch". 
Ben's video series is based on the "SAP-1 (Simple As Possible 1)" computer, described in "Digital Computer Electronics" 
book by Albert Malvino and Jerald Brown, first released in 1977. 

And like thousands of others, I wanted to build my own. Partly to learn a few things, but above all for fun. 
But I also wanted a few differences: 
  - Use wire-wrapping instead of breadboards. As I could only work on it mostly on weekends and in my spare time,
    I wanted it to be longer-lasting so I could put it away easily and pull it out without first spending time to
    find which wires have been dislodged to get it back working again. 
  - Stay closer to Malvino's original design for the SAP-1. 
  - Add some blinkenlights to visualize:
    - LED bar graphs for W-bus, Accu, B-register, Output-register, Instruction register 
    - LEDs for the control signals (La, Ea, Lb, Eb, Ep, CE ...) and the Program Counter 
    - the ring counter indicating the stage of the Fetch/Execute cycle 
    - the instruction decoder 
  - Added a dual 7-segment display to visualize the W-bus content in HEX-format instead of in binary via LED bar graph.

In short, I wanted it to be much more of a visual CPU that can show which signal gets activated and what it triggers 
in various parts of the CPU. Because I wanted the wiring to be visible, I did not use wire-wrap sockets and wire on the 
bottom of the perfboard. Instead, I soldered pin headers next to each row of IC pins so I had access to each pin on the 
top and wire-wrapped from pinheader pin to pinheader pin. 

Most important specs: 
  - 4 bits address bus with 16 bytes RAM memory and an 8 bits data bus 
  - 4 instructions: Load, Add, Sub and Out
  - Opcodes is the most-significant-nibble (top 4 bits) and memory location is the least (bottom 4 bits) 
  - Clock signal can be single stepped, or auto-run with variable clock speed (up to a few dozen Hz)
  - Done using a mix of various 74-series ICs (LS, F ...) and implemented on a 20cmx30cm (8"x12") perfboard.

