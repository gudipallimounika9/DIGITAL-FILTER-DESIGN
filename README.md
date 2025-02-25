# DIGITAL-FILTER-DESIGN
COMPANY NAME: CODETECH IT SOLUTIONS PVT.LTD

NAME: GudipalliMounika

INTERN ID: CTCGUG

DOMAIN: VLSI

BATCH DURATION:JAN 20th,2025 to MARCH 20th,2025

MENTOR NAME:NEELA SANTHOSH

DESCRIPTION: The filter is designed to process a signed 16-bit input signal (x_in) and produce a signed 32-bit output signal (y_out). The design includes a shift register for storing input samples and a set of fixed filter coefficients.

Implements a 5-tap FIR filter with predefined coefficients.
Stores past input samples in a shift register.
Computes the convolution sum using a multiply-and-accumulate (MAC) operation.
Resets internal states when the reset signal is asserted.

Operation of FIR Filter
(1) Reset Condition
When reset = 1, the output y_out is cleared to 0, and all stored input values are reset to 0.

(2) Shift Register Operation
New input (x_in) is stored at x[0].
Older values are shifted to the right.

(3) FIR Convolution Computation
Computes convolution sum
Uses a temporary register (temp_sum) to correctly accumulate the sum before assigning it to y_out

Testbench Module (tb_fir_filter)

Functionality:

Generates a clock (clk) signal.

Controls the reset (reset) signal.

Applies test input values (x_in) to the FIR filter.

Stops the simulation after a sequence of test values.

Key Components:
(a) Clock Generation
Generates a clock signal with a period of 10 time units.

(b) Stimulus Generation
Initial conditions: Reset is asserted for 20 time units.
Applies a sequence of values (x_in) every 10 time units.
Stops simulation after all test values are applied.

