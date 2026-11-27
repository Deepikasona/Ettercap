# ARP Detection Method – Member 3

## Overview
This project section demonstrates a simple check for a possible gateway MAC address change.

## Detection logic
1. Record a trusted gateway IP-to-MAC reference from the project laptop.
2. Enter the current gateway MAC value for comparison.
3. Compare the current MAC with the trusted baseline.
4. If they match, display `NETWORK NORMAL`.
5. If they differ, display a warning and add an alert to the report.

## Test results
- Normal test: the current MAC matched the trusted MAC, so the notebook displayed `NETWORK NORMAL`.
- Suspicious test: a different MAC was entered as simulated test data, and the notebook displayed a warning.
- Final report: the simulated mismatch produced one alert.

## Important limitation
The gateway details were manually recorded from the Windows laptop and entered into Google Colab. Colab cannot directly read the laptop's local ARP neighbour table. The changed MAC value was simulated. Therefore, this implementation demonstrates comparison logic; it is not live ARP monitoring, packet capture, or proof that an actual attack occurred.
