# Silent CSV Read Failure in R

This repository demonstrates a common, yet subtle, error in R when reading CSV files: silent failure when the file does not exist. The script `bug.R` attempts to read a CSV. If the file is missing, no error is reported, causing unexpected downstream issues.

The solution, `bugSolution.R`, demonstrates how to robustly handle this using `tryCatch` to gracefully manage potential file reading errors.

## How to Reproduce

1.  Clone this repository.
2.  Run `bug.R`.  Note that if `my_data.csv` doesn't exist, the script will run without error, but `data` will be null or empty, resulting in errors in further processing steps.
3.  Run `bugSolution.R` to see the improved error handling.