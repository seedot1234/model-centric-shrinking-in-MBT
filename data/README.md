# raw shrinking data

These are the results for shrinking test cases using the shrinking algorithms in the thesis. The CSV files are structured as follows:

First, there is a comment block. These are the lines that start with `#`. The comment block contains general information on the shrinking process.

- **Shrunk traces:** 10  
  The number of test cases that were shrunk.

- **Start total, inputs:** 2276, 1732  
  The number of total steps (e.g. input + output) in the traces that were shrunk, and only the number of inputs.

- **Start:** [56, 546, 86, 22, 130, 528, 39, 236, 482, 151]  
  The length of each individual test case before shrinking.

- **Start inputs:** [43, 411, 63, 17, 101, 411, 28, 180, 366, 112]  
  The length in inputs only.

- **Start max, min, avg:** 411, 17, 173.2  
  The minimum, maximum, and average length of traces before shrinking (inputs only).

Next, there is a header with the name of each column:

shrinker, time, times, nr_tests, nr_steps, steps, nr_inputs, inputs, end_max, end_min, end_avg, end, end_all_max, end_all_min, end_all_avg, end_all, time_step


- **shrinker:** A list of the shrinkers that were used.
- **time:** The total time of the shrinking process.
- **times:** An array with the time it took to shrink each individual test case.
- **nr_tests:** The number of test cases executed in the shrinking process.
- **nr_steps, steps:** Total number of steps (inputs + outputs) and the steps for each test case shrunk.
- **nr_inputs, inputs:** Total number of interactions with the SUT (inputs) and inputs for each test case shrunk.

The columns afterwards contain the maximum, minimum, and average size of the shrunk traces at the end measured in number of inputs in the trace (e.g. interactions with the SUT). The columns with the `_all_` infix contain the same information, but counting both inputs and outputs.

The final line contains a calculation for the time that was needed per interaction with the SUT.

## Files
There are three folders, each containing the raw data of a different experiment: smartdoor, koopman, and ATM. Per experiment, the data are grouped per bug. Smartdoor contains 8 bugs, of which bug 01, 02, 04, 05, 06, and 07 are state bugs. The other bugs are trace bugs. Koopman contains 10 bugs, of which bug 03 and 06 are state bugs, the others being trace bugs. ATM contains 5 bugs; 01, 03 and 04 are state bugs and the others are trace bugs.

## Acknowledgments
This dataformat is taken from Lars Meijer: https://github.com/Lars-Meijer/sts-shrinking-results.
