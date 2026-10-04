# UAIS

This article provides executables of software and datasets used in our research for Fast High Utility Itemset Analytics with Sliding Window-Oriented Indexed Lists.

The executables include the software of UAIS, SHUPM, SHU-Growth, SHAUPM-A, IIMHAUP-A, PIHUPM, PULM, PIHAUPA-A and the datasets of Accidents, Chain-store, AQ, AEP, EShop, OnlineRetail, and T10I4D200K—T10I4D1000K.

All executables were compiled to run on 64-bit architectures.

Please refer to the following guide:

1. Note that the names of the executables match their corresponding approach names.

2. The parameters of the executables are as follows:

 for UAIS, SHUPM, SHU-Growth, SHAUPM-A, IIMHAUP-A
```bash
[0]          [1]            [2]                 [3]                     [4]          [5]           [6]
[Executable] [Threshold(%)] [Utility Data Path] [Transaction Data Path] [Batch Size] [Window Size] [Out File Path]

```

 for PIHUPM, PULM, PIHAUPA-A
```bash
[0]          [1]        [2]        [3]                 [4]                     [5]          [6]           [7]
[Executable] [Thr_u(%)] [Thr_l(%)] [Utility Data Path] [Transaction Data Path] [Batch Size] [Window Size] [Out File Path]

```

3. Next, the file name and the parameters of each dataset are as follows:

| Dataset     | Number of Transactions | Number of Items | \|T\|.avg |
| ----------- | ---------------------- | --------------- | --------- |
| Accidents   | 340,183                | 468             | 33.808    |
| Chain-store | 1,112,949              | 46,086          | 7.2       |
| AQ          | 9,326                  | 130             | 11.252    |
| AEP         | 19,735                 | 78              | 26.0      |
| EShop       | 165,474                | 24,564          | 13        |
| OnlineRetail| 530,104                | 7,918           | 6.8       |
| T10I4DxK    | 200,000-1,000,000      | 1,000           | 10        |

4. For example
```bash
UAIS 0.7 ..\Data\utilAQ.txt ..\Data\AQ.txt 1600 3 out\out.txt
```
will run UAIS on AQ, with the threshold set at 0.7%
```bash
PIHUPM 0.7 0.1 ..\Data\utilAQ.txt ..\Data\AQ.txt 1600 3 out\out.txt
```
will run PIHUPM on AQ, with the upper threshold and lower threshold set at 0.7% and 0.1%

5. The output directory "/out" is required for writing result patterns for all algorithms.