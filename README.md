# Rust Undefined Behavior Example

This repository demonstrates a simple Rust program that exhibits undefined behavior due to unsafe manipulation of a vector's internal data. The code directly modifies the vector's underlying memory using `as_mut_ptr()`, violating Rust's memory safety rules.

## Bug Description
The `bug.rs` file contains a function that uses `as_mut_ptr()` to modify the first element of a vector.  Because this bypasses Rust's safe memory management mechanisms, the resulting behavior is undefined and unpredictable.

## Solution
The `bugSolution.rs` file demonstrates a safe way to modify the vector's element using indexing.

## How to Reproduce
1. Clone this repository.
2. Navigate to the repository's directory.
3. Run the code using `rustc bug.rs && ./bug`.
4. Observe the output and potential runtime errors.
5. Compare the outcome with the safe version in `bugSolution.rs`.
