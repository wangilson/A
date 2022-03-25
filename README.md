# Repository of A

Prerequisites
To use A,we need the following tools installed

+ llvm-10.0.0
+ boost 1.71

## Usage and Example
1. Uncompress the lib
```
cd A_bin
unzip lib.zip
```
2. Currently, we receive llvm-IR *.bc as input.
```
 cd A_bin
 A [input.file] -t-e main -i-e [isr_fun1,isr_fun2...] -i-p [isr_priority1,isr_priority1...] -o [output.file]
```
3. We use the example.bc to illustrate the tool-chain.
```
  A ../racebench/svp_simple_001/svp_simple_001.bc -t-e main -i-e svp_simple_001_001_isr_1,svp_simple_001_001_isr_2 -i-p 1,2 -o output.file
```
## Note
interrupt number of each ISR is the same as the order in list.
