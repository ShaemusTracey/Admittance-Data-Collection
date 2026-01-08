# Admittance-Collection

MATLAB script for automating the admittance measurement for both piezoelectric channels of a Traveling Wave Ultrasonic Motor (TWUSM) using a frequency sweep analysis.

## Overview

Automates frequency sweep testing of TWUSM stators by controlling a Rigol DG1022 waveform generator and DS1052/DS1104 oscilloscope to collect voltage data for admittance calculations.

## Requirements

**Hardware:**
- Rigol DG1022 Arbitrary Waveform Generator
- Rigol DS1052 or DS1104 Oscilloscope

**Software:**
- MATLAB with Instrument Control Toolbox
- NI-VISA drivers

## Configuration

Edit these parameters in the script:

```matlab
min_F = 30000;      % Start frequency (Hz)
max_F = 50000;      % End frequency (Hz)
step = 10;          % Step size (Hz)
Vpp = 6;            % Peak-to-peak voltage (V)
scope = DS1104;     % Select your oscilloscope: DS1052 or DS1104
```

## Output

Results stored in MATLAB workspace:
- `freq` - Frequencies tested
- `V1`, `V2` - Voltage measurements from both channels
- `T` - Time array
- `raw_Data_CH1`, `raw_Data_CH2` - Raw oscilloscope data

## Resources
More infortmation about the project, electrical setup, and expected results can be found [here](https://shaemustracey.github.io/Admittance_Data_Collection_Page.html).