# Time and Energy Analysis of Sorting Algorithms

This application measures the runtime and energy consumption of sorting algorithms in C++

## Sorting algorithms analyzed
@TODO list...

## How are we measuring energy consumption?
The RAPL library, implemented in C, is adapted from an independent research project that Rutvik and Alejandro are working on for Professor Yu David Liu. @TODO: link to the jRAPL repo

RAPL stands for Running Average Power Limit, a way of monitoring and controlling a computer's energy levels. It works on Intel processors by reading and writing the Model Specific Registers (MSRs). In this project, we only directly access one function from the library, EnergyStatCheck(), which returns total energy consumption. We call the function before and after running our sorting algorithms and take the difference in readings.
EnergyStatCheck() returns energy readings for three different power domains: DRAM, CPU, and Package. Package is the entire CPU socket. Our algorithms will therefore be measured with respect to energy consumption in each of these three power domains.

## How are we measuring runtime?
Using std::chrono we can timestamp before and after a function runs and take the difference to measure the elapsed time.
@TODO -- milton, elaborate on the exact implementation

## Performance analysis implementation
Our sorting algorithms are accessed in an array of function pointers. We iterate through pass each algorithm into a performance analysis function @TODO what's it called?
The performance analysis function ........

## Graphing results
