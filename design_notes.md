- verilog is a hardware description language
- developed by gateway design automation in 1980 and later acquired by cadence systems
- it is also used for verification purposes
- it supports abstraction from structural to behavioural
- it is used for both simulation based and synthesis based design
- apple and intel series chips are designed using verilog and it's successor system verilog
- before verilog the language used for this purpose are VHDL (VHSIC HDL){very high speed integrated circuit hardware description language}
- the previous before this abel(advanced bollean expression language)
# which makes the verilog better ?
- simpler syntax 
- better support for behavioural modelling - allows from gate level to behavioural level
- high level of abstraction - describing digital circuits using modules and ports
- better tool support
# future impacts other than verilog
- HLS where it helps to go around many approach of design in short span of time
- some new progtramming languages are chisel and myhdl
# hardware schematic
- hardware schematic is a diagram that shows how the combinational gates are connected to attain an harware block
# verilog structure
- module definition
- list of input and output ports
- instantiation
- behavioural code
# ASIC DESIGN FLOW
- ASIC design flow is the systematic methodology for transforming a chip concept from initial requirements through architecture, RTL design, verification, synthesis, physical implementation, and validation--a multi-stage process used by semiconductor companies to develop custom integrated circuits 

- After rtl design, verification and synthesis, LEC(logic Equivalence plays a major role comparing the syntehsised with rtl using synopsys formality, cadence conformal)

- next step is placement and routing
# verilog basics
- comments can be used are // and /* jilnwkjsk */
- in verilog the spaces in the string also considered as the character
- operators unary, binary, conditional
- number format [size]'[base_format][number]
- numbers with unsized formats are considered with the default size where the number is considered as decimal
- signed number sign [size]'[base_format][number]
- strings are enclosed with quotes
- identifiers are variables other than reserved words
- keywords - reserved words
- a module is a block of verilog code that does a functionality
- a top level module is the one which contains other sub modules
- ports are set of signals that act as input and output to the modules
- port types input, output and inout
- port syntax [direction] [data_type] [bit_width] [name] [bit_depth]
- default the ports are unsigned if it is required it can be assigned signed
- if the type is not declared directly in ports it can be redeclareds
- inout always should have a tristate logic
- unconnected ports in instantiation will always have high impedance
- nets are used to drive the data and not to hold the data
- wire with three to more bits driving is referred as a vector
- other data types reg used to store data but not same as flipflop it can also be used for combinational circuits - not synthesizable
- integer - to store 32 bit data type - not synthesizable
- time - unsigned 64 bits wide used to store simulation time quantities - not synthesizable
- realtime is a floating point time - not synthesizable
- real - 64 bit floating point for arithmetic calculations - not synthesizable
- it saves the string from lsb to msb with respect to the memory allowed
- a datatype without a range specification is scalar
- with range specification is vector
- bit select - selection of bit through indexing in the data
- part select - if it is from msb to lsb the part selection should also be in same idealogy
- tri reg net driven state - takes the value of the driver
- capacitive state - when it attains the high impedance state it maintains the previous value
- tri0 acts as a pull down resistor (open source logic)
- tri1 acts as a pull up resistor (open drain logic)
- uwire - allows only a single wire
- supply0, supply1 are used for the vcc, gnd
- avoid multiplication,division, modulus and power operators directly
- multiplication, division and modulus are high complexer
- power is not synthesizable
- for single bit relational operators are developed into a magnitude comparator
- for multibits it uses ripple comparison or tree comparison logic
- and truth table z&z- x any highimpedance or unknown with any other than 0 is x
- or truth table 0|z is x
# operator precedence table
- 1 - unary not
- 2 - power
- 3 - mul,div and mod
- 4 - add,sub
- 5 - shifts
- 6 - comparison
- 7 - equality
- 8 - bitwise and
- 9 - bitwise xor,xnor
- 10 - bitwise or
- 11 - logical and
- 12 - logical OR
- 13 - ternary

# measures need to be done

- good design practice involves avoid x and z states in critical logic
- all the arithmetic operations will not be synthesized for real and real time types
- -m where for signed integer it stores the 2's complement of the value
- if the input is 8 bit and output is 8 bit for the sum, the carry will be truncated
- division by zero leads to the x undefined value
- parameters are constants defined at elaboration time
- the calculations made with only parameters will be executed in elaboration/compilation time
- where the constants will be synthseized directly
- if any one operand is unsigned the overall operation is considered as unsigned
# Concatenation Operator
- multi bit wires and variable can be clubbed together to form a bigger multi net using concatenation or set membership opeartor
- replication operator where it's synatax is {no_of_times{variable}}
- nested replication is also allowed
- 

