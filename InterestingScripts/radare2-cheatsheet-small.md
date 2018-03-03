# Cheatsheet

dynamic analysis with `-d`
static analysis without `-d`

## Must run command
|command|description|
|----|---|
|`aaa`|analyse all
|`s sym.main`| seek main function
|`pdf`| disassemble

## Some r2 Representations
`sym.main`              => local function
`sym.imp.printf`        => imported function
`local_4h`              => same as `rbp-0x4`

## Useful static analysis
|command|description|
|----|---|
|`VV`| Graph
|`px` / `pxw` / `pxq` | hexdump|

## Useful debugging (dynamic)

|command|description|
|----|---|
|`db main`| break main|
|`dc`| continue |
run above before going into Visual Debug mode (V -> p -> p).

    Visual Debug mode will show registers + disass + highlightings

Command Mode with `:`
|command|description|
|----|---|
|`ds`| step|
|`dso`| step over|

Back to visual mode with [Enter]
`s` to step
[shift] + r  to randomize colors (easier to see)

## View registers and data at addresses

Similar to GDB's examine `x/s` or `x/d` or `x/x`
|command|description|
|----|---|
|`ps @ addr/reg/reg+offset`| print string at the address |
|`pfi @ addr/reg/reg+offset`| print integer at the address |
|`pfx @ addr/reg/reg+offset`| print hex at the address |

View Registers
|command|description|
|----|---|
| `dr` | see all register (similar to GDB's `info re