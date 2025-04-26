# SimpleComputer

A CPU simulator with an integrated SimpleBasic interpreter. This project simulates a basic computer architecture with memory management, instruction execution, and terminal-based UI.

## Features

- Memory visualization and manipulation
- Basic CPU operations simulation
- SimpleBasic interpreter
- Terminal-based user interface
- Accumulator and instruction counter
- Interactive memory cell editing

## Controls

### Navigation
- `↑` `↓` `←` `→` - Move cursor between memory cells
- `Enter` - Edit selected memory cell
- `ESC` - Exit program

### Program Execution
- `r` - Run program
- `t` - Execute one step (trace mode)
- `i` - Reset computer

### Memory Operations
- `l` - Load program from file
- `s` - Save program to file

### Registers
- `F5` - Set accumulator value (in hex)
- `F6` - Set instruction counter value

### Value Input
- `0-9` - Decimal digits
- `a-f` - Hexadecimal digits
- `+/-` - Set value sign when editing

## Building

```sh
make
```

## Running

```bash
# Run the SimpleComputer simulator
./bin/app

## Project Structure

```
simplecomputer/
├── console/          # Terminal interface implementation
├── include/          # Header files and common definitions
├── myALU_CU/        # Arithmetic Logic Unit and Control Unit
│   ├── alu.c        # ALU operations
│   └── cu.c         # Control Unit logic
├── myBigChars/      # Big character display for UI
├── myReadkey/       # Keyboard input handling
├── mySimpleComputer/ # Core computer simulation
├── myTerm/          # Terminal manipulation utilities
├── simpleassembler/ # Assembly language implementation
└── simplebasic/     # BASIC language interpreter
```

## Technical Details

The simulator implements:
- 100 memory cells (00-99)
- 16-bit word size
- Basic arithmetic operations
- Conditional and unconditional jumps
- I/O operations
- Simple assembly language
- BASIC language subset

### Memory Layout
```
+------------------+
|    Memory (99)   |
|        ...       |
|    Memory (00)   |
+------------------+
| Instruction Ptr  |
| Accumulator      |
+------------------+
```
