# NSDOS Leaf EDitor
An ED (GNU + CP/M) inspired editor for the NorthStar Graphics Disk Operating System version 1.0.0AQ

I'd recomend having syntax highlighting for the intel 8080's pnemonics, and tabsize of 8. Though it's perfectly acceptable to view it with no highlighting.
wrote a simple vim syntax file for it, [here](https://github.com/sage-etcher/vim-i8080-syntax), but for other edittors you're on your own

## Assembling Information

The assembly uses intel 8080 pnemonics and is designed to assemble using CP/M's `ASM.COM` and `LOAD.COM`. All other methods of assembly are untested, and as such, may require modifications to directive or comments declarations.

__note:__ getting the assembled binary off of CP/M and onto NSDOS can be difficult. One, non-ideal, method is to write the file as hex, using `MC000` (nsdos monitor program) and then save that chunk of memory into the required file.

supplied are a short description of directives used

| Directive | Description |
|:--------- |:------------|
| `ORG` | set program origin point |
| `END` | end of source code |
| `EQU` | pre-processor constant |
| `DB` | define Byte(s) |
| `DW` | define Word(s) |
| `DS` | declare _n_ Bytes of data |
| `;` | comment specifer |
| `:` | define a label |
| `$ (in EQU)` | current memory location |
| `$` | empty spacer, helpful in numbers and labels |
| `!` | virtual newline |
| `+-/*` | preprocessor arithmatic |
| `''` | string specifier, CANNOT be doube quotes |

number definitions as used within this project

| Base | Definition | Example (24 decimal) |
|:---- |:---------- |:-------------------- |
| Hex (16) | 0<i>xx</i>H | 018H |
| Dec (10) | <i>xx</i> | 24 |
| Oct (8) | 0<i>xxxx</i>Q | 030Q |
| Bin (2) | 0<i>xxxx</i>$<i>xxxx</i>B | 00001$1000B |

## License (Apache Versoin 2.0)

Copyright 2023 Sage I. Hendricks  

Licensed under the Apache License, Version 2.0 (the "License");  
you may not use this file except in compliance with the License.  
You may obtain a copy of the License at  

&nbsp;&nbsp;&nbsp;&nbsp;<http://www.apache.org/licenses/LICENSE-2.0>  

Unless required by applicable law or agreed to in writing, software  
distributed under the License is distributed on an "AS IS" BASIS,  
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  
See the License for the specific language governing permissions and  
limitations under the License.  

