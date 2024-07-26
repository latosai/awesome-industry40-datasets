# CNC Mill Tool Wear

| Parameter | Value |
| --- | --- |

## Data Set Information
A series of machining experiments were run on 2" x 2" x 1.5" wax blocks in a CNC milling machine in the System-level Manufacturing and Automation Research Testbed (SMART) at the University of Michigan. Machining data was collected from a CNC machine for variations of tool condition, feed rate, and clamping pressure. Each experiment produced a finished wax part with an "S" shape - S for smart manufacturing - carved into the top face, as shown in `test_artifact.jpg` (included in the dataset).  

General data from each of the 18 different experiments are given in `train.csv`  Time series data was collected from the 18 experiments with a sampling rate of `100 ms` and are separately reported in files `experiment_01.csv` to `experiment_18.csv`. Each `experiment_xx.csv` file consists of 48 columns and the number of each row is from `experiment_01.csv` to `experiment_18.csv` (1056, 1669, 1522, 533, 463, 1297, 566, 606, 741, 1302, 2315, 2276 , 2234, 2333, 1382, 603, 2151, 2254). Time series data from 18 experiments is collected at a sampling rate of 100 ms.   


| Data Set          | Number of row | Data Set          | Number of row |
| ----------------- | ------------- | ----------------- | ------------- |
| experiment_01.csv | 1056          | experiment_10.csv | 1302          |
| experiment_02.csv | 1669          | experiment_11.csv | 2315          |
| experiment_03.csv | 1522          | experiment_12.csv | 2276          |
| experiment_04.csv | 533           | experiment_13.csv | 2234          |
| experiment_05.csv | 463           | experiment_14.csv | 2333          |
| experiment_06.csv | 1297          | experiment_15.csv | 1382          |
| experiment_07.csv | 566           | experiment_16.csv | 603           |
| experiment_08.csv | 606           | experiment_17.csv | 2151          |
| experiment_09.csv | 741           | experiment_18.csv | 2254          |
|                   |               | Train.csv         | 18            |

## Attribute Information
- `Train.csv`       

| Inputs(features)     | Description                                                  | Outputs(predictions)     | Description                                                  |
| -------------------- | ------------------------------------------------------------ | ------------------------ | ------------------------------------------------------------ |
| No.experiment number | -                                                            | tool_condition           | label for unworn and worn tools                              |
| material             | wax                                                          | machine_completed        | indicator for if machine was completed without the workspace moving out of the pneumatic vise |
| feed_rate            | relative velocity of the cutting tool along the workpiece(mm/s) | passed_visual_inspection | indicator for if the workpiece passed visual   inspection, only available for experiments where machining was completed |
| clamp_pressure       | pressure used to hold the workpiece in the wise(bar)         | -                        |                                                              |

The 'tool_condition' variable indicates whether the tool is unworn or worn.

## References
