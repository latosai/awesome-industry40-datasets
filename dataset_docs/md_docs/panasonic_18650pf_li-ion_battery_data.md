# Panasonic 18650PF Li-ion Battery Data

| Parameter | Value |
| --- | --- |
| Data Set Characteristics | Attribute Characteristics | Real |
| Attribute Characteristics | Real |
| Associated Tasks | Number of Instances	| |
| Number of Instances | Number of Attributes | |
| Number of Attributes | Date Donated | 2018-06-20 |
| Date Donated | 2018-06-20 |
| Source | Dataset size | 200 MB (compressed) |
| Dataset size | 200 MB (compressed) |

## Data Set Information
A brand new 2.9Ah Panasonic 18650PF cell was tested in an 8 cu.ft. thermal chamber with a 25 amp, 18 volt Digatron Firing Circuits Universal Battery Tester channel.

A series of tests were performed at five different temperatures, as follows (battery charged after each test at 1C rate to 4.2V, 50mA cut off, with battery temperature 12degC or greater):

1. Cycled at 1C rate at 25degC ten times to break it in (this data is not included)
2. C/20 discharge and charge test
3. Five pulse discharge HPPC test (0.5, 1, 2, 4, 6C) performed at 100, 95, 90, 80, 70..., 30, 25, 20, 15, 10, 5, 0 % SOC.  The logged data file only includes the pulses, and does not include the subsequent discharges between the pulses, refer to the amp-hour data to determine the SOC for each pulse set.  The discharges between pulses are included in another file, with "dis5_10p" in the name, in case this data is needed.
4. EIS test performed from 1mHz to 100, 95, 90, 80, 70..., 30, 25, 20, 15, 10, 5, 0 % SOC.
5. Series of nine drive cycles performed, in following order: Cycle 1, Cycle 2, Cycle 3, Cycle 4, US06, HWFET, UDDS, LA92, Neural Network (NN).  Cycles 1-4 consist of random mix of US06, HWFET, UDDS, LA92, and Neural Network drive cycels.  Neural Network drive cycle consists of combination of portions of US06 and LA92 drive cycle, and was designed to have some additional dynamics which may be useful for training neural networks.  The drive cycle power profile is calculated for an electric Ford F150 truck with a 35kWh battery pack scaled for a single 18650PF cell.
6. Steps 3 through 5 are repeated for ambient temperatures of 25degC, 10degC, 0degC, -10degC, and -20degC, in that order. For tests with ambient temperature below 10degC, no regen is included in the test.  The drive cycle tests are terminated when voltage first hits 2.5V for 25degC and 10degC and after 2.32Ah (80% DOD), 2.03Ah (70% DOD), and 1.74Ah (60% DOD) have been discharged at 0degC, -10degC, and -20degC respectively.
7. The nine drive cycles are repeated ("-20degC Trise" folder) with a starting chamber temperature of -20degC, which is then allowed to drift upwards such that the battery temperature rises up to 10 or 20degC during the drive cycle.  These tests allow for testing battery models or SOC algorithms with varied temperature drive cycle tests.  The battery ages as more tests are performed though, so these test results may not perfectly compare models developed from earlier tests.
8. Cycles 1 through 3 are repeated ("-20degC Trise with pause" folder) with an ambient temperature starting at -20degC, which is then allowed to drift upwards such that battery temperature rises as high as 25degC.  Each cycle has a 1, 2, or 3 hour pause inserted in the middle.  The cycles and charges are saved in a single contiguous file to allow for evaluation of battery models or SOC algorithms over a contiguous data set with varied temperature.
9. The nine drive cycles are repeated ("10degC Trise" folder) with a starting ambient temperature of 10degC, similar to that described in step 7.
10. Cycles 1 through 4 are repeated ("10degC Trise with pauses")with a starting ambient temperature of 10degC, similar to that described in step 8.  These cycles include regen power though, since temperature is greater than 10degC.
11. The battery is cycled ten times at 25degC at a rate of 1C ("C20 OCV Test_end_of_tests" folder).  This is followed by two reference capacity tests performed at 1C, which show that the 1C battery capacity has fallen from 2.8Ah to 2.3Ah after the series of tests performed (approximately 110 cycles).

## Attribute Information
- TimeStamp (timestamp in MM/DD/YYYY HH:MM:SS AM format)
- Voltage (measured cell terminal voltage, sense leads welded directly to battery terminal)
  Current (measure current in amps)
- Ah (measured amp-hours, with Ah counter reset before each charge, test, or drive cycle)
- Wh (measured watt-hours, with Wh counter reset after each charge, test, or drive cycle)
- Power (measure power in watts)
- Battery_Temp_degC (battery case temperature, at middle of battery, in degrees Celsius measured with a thermocouple, measurement corrected for thermocouple offset at lower temperatures)
- Time (time in seconds, starts at zero at beginning of each data file)
- Chamber_Temp_degC (measured chamber temperature in degrees Celsius)

## References
