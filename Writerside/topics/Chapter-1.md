# Verilog

## Generalities
ASIC - Fixed-function hardware, application-specific-integrated-circuit\
FPGA - Flexible-function hw, field-programmable gate array

ASIC & FPGA steps:
- Design
- Simulation
- Place and route
- Static Timing analysis
- Lab debug

FPGAs allow us to retrace back to Place & Route, without the need to re-start the process.

## Verilog
```assign a = b;``` -> Assign the value of b to a, where in can be a signal, function or operation. Out is any signal
declared.\
```//comment or /**/``` -> self-explanatory
```if (condition) event``` -> if statement

## Logical operations
```NOT = !```, eg ```assign a = !b;```\
```AND = &&```, eg ```assign c = a && b;```\
```OR = ||```, eg ```assign c = a || b;```\
```XOR = ^```, eg ```assign c = a ^ b;```\
Chaining operations: ```assign delta = ((a && b) | c) ^ d```

## Bitwise operations (just like C)
```Bitwise and = &```, eg ```assign a = !b;```\
```Bitwise or = |```, eg ```assign a = !b;```

### Modules
Represent "programs" associated with FPGAs
```
module top(input clk_25mhz,
           input [6:0] btn,
           output [7:0] led,
           output wifi_gpio0);

    wire i_clk;

    // Tie GPIO0, keep board from rebooting
    assign wifi_gpio0 = 1'b1;
    assign i_clk= clk_25mhz;
    reg [7:0] o_led;
    assign led= o_led;
    localparam ctr_width = 32;
    reg [ctr_width-1:0] ctr = 0;

    always @(posedge i_clk) begin
               ctr <= ctr + 1;
          o_led[7] <= 1;
          o_led[6] <= btn[1];
        o_led[5:0] <= ctr[23:18];
    end

endmodule

```

`timescale [unit]/[precision]`: sets timescale associated to the program. Associated values are `s`, `ms` ... `fs`.\
`module block`: contains the port list, with input and output ports\
`#(parameter)`: if marked with #, represents a parameter list, which can be used to define parameters used.

## Parameters
- Parameters help clean up code
- Parameters can be integers, strings, or types (similar to typedef, one can write) `#(parameter type LED = logic unsigned [5:0]`

## Data types
- `logic` : (true, false, x for undefined, z for tri-state)
- `bit`   : stores a 1 or a zero
- `byte`: 8 bits
- `shortint`: 16 bits
- `int`: 32 bits
- `longint`: 64 bits

## Arrays
- Packed and unpacked types
- Packed: `bit [31:0] dword`
- Unpacked: `bit [32] dword`

### Query functions
- `$left(array, [dimension])`: dimensions of an array
- `$right(array, [dimension])`: leftmost value
- `$high(array, [dimension])`: largest value in the dimension's range
- `$low(array, [dimension])`: smallest value in the dimension's range
- `$size(array)`
- `$bits()`: number of bits used
- `$clog2()`: size of an array that can hold the number of items passed

### Array assigning
- `logic [7:0] data;
assign data = '1;` -> gets filled with 1
- `logic [7:0] data;
    assign data = '0;` -> gets filled with 0
- `logic [7:0] data;
  assign data = 'z;` -> gets filled with z
- `logic [7:0] data;
    assign data = 0;` -> first 32 bits set to 0 (**default size is 32!**)

## Number formats
- Signed & unsigned: `bit [un]signed[31:0] [un]signed_vector;` creates a value, with two's complement

## Concatenation
- Done using the `{}` operator: add and replicate bits
- `{1'b0, unsigned_vect}` merges the values, `{2{unsigned_vect}}` creates two concatenated copies of unsigned_vect

## Casting
- Done via the `signed'` keyword

## Functions
- `function [data:size] name(input [data:size] arg);`