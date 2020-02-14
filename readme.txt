Data Set: FD001
Train trjectories: 100
Test trajectories: 100
Conditions: ONE (Sea Level)
Fault Modes: ONE (HPC Degradation)

Data Set: FD002
Train trjectories: 260
Test trajectories: 259
Conditions: SIX 
Fault Modes: ONE (HPC Degradation)

Data Set: FD003
Train trjectories: 100
Test trajectories: 100
Conditions: ONE (Sea Level)
Fault Modes: TWO (HPC Degradation, Fan Degradation)

Data Set: FD004
Train trjectories: 248
Test trajectories: 249
Conditions: SIX 
Fault Modes: TWO (HPC Degradation, Fan Degradation)



Experimental Scenario#方案、设想

Data sets consists of multiple multivariate time series（多变量时间序列）. Each data set is further divided into training and test subsets. Each time series is from a different engine ?i.e., the data can be considered to be from a fleet of engines of the same type(可以认为数据是来自同一类型的发动机). Each engine starts with different degrees of initial wear and manufacturing variation which is unknown to the user（初始磨损程度和制造差异）. This wear and variation is considered normal, i.e., it is not considered a fault condition. There are three operational settings that have a substantial effect (实质性影响)on engine performance. These settings are also included in the data. The data is contaminated with sensor noise.（被传感器噪声污染）

The engine is operating normally at the start of each time series, and develops a fault at some point during the series. In the training set, the fault grows in magnitude until system failure(故障规模增大直到系统GG). In the test set, the time series ends some time prior to system failure. The objective of the competition is to predict the number of remaining operational cycles before failure in the test set, i.e., the number of operational cycles after the last cycle that the engine will continue to operate. Also provided a vector of true Remaining Useful Life (RUL) values for the test data.
                                                                                                                                                                                                                                                                                                                                     在测试集中，时间序列在系统故障之前的某个时间结束。竞赛的目的是预测试验装置故障前的剩余运转循环数，即发动机将继续运转的最后一个循环后的运转循环数。还为测试数据提供了真实剩余使用寿命（rul）值的矢量。
The data are provided as a zip-compressed text file with 26 columns of numbers, separated by spaces. Each row is a snapshot of data taken during a single operational cycle, each column is a different variable. The columns correspond to:  每一行是在单个操作周期中获取的数据的快照，每一列是不同的变量。这些列对应于：
1)	unit number
2)	time, in cycles
3)	operational setting 1
4)	operational setting 2
5)	operational setting 3
6)	sensor measurement  1
7)	sensor measurement  2
...
26)	sensor measurement  26


Reference: A. Saxena, K. Goebel, D. Simon, and N. Eklund, 揇amage Propagation Modeling for Aircraft Engine Run-to-Failure Simulation? in the Proceedings of the Ist International Conference on Prognostics and Health Management (PHM08), Denver CO, Oct 2008.
