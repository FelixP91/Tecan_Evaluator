# Tecan_Evaluator
Evaluates kinetic measurements by a TECAN photometer.

## Description

This code takes the output file (.xlsx) generated by a TECAN photometer and calculates the maximum slopes for each measurement. It is assumed that fluorescence/absorption rises over time due to enzymatic activity. Several measurements can be present per sheet and several sheets can be present per file. First, curve smoothing is applied using the Savitzky–Golay filteer to kinetic data to reeduce the noise. Then, the averaged (to increase robustness) maximum slopes for a user-defined time interval are calculated. The maximum slopes are stored in a seperate output file generated by running the code. An example-TECAN file is provided (TECAN_output_file.xlsx) which can be used for running the code (input_file= path to TECAN_output_file.xlsx).

<div style="padding:2em">
<img src="https://github.com/FelixP91/Tecan_Evaluator/blob/main/Figure_TECAN_analysis.png?raw=true" width="1000" align=center>
 Example of maximum slopes (orange lines) calculated for three kinetic measurements (blue lines, smoothed by SavGol filter). The length of the slope (orange line) is user-defined.
 x_axis= time of measurement in seconds, y_axis= fluorescence intensity.
</div>


## Project

This repository contains two main files:

* /Evaluation_TECAN_files.py
  * code for running the evaluation of a TECAN output file (.xlsx)
* /TECAN_output_file.xlsx
  * example file that acn be used for running the code (


## Requirements

Required packages to run this code are:

* python: pandas, scipy, numpy, matplotlib.


## Contact

Dr. Felix Panis, felix.panis@univie.ac.at
