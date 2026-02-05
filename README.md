ABSTRACT

Research in anomaly detection in Smart Meter time-series data is, generally, evaluated using synthetically created anomalies. These anomalies often fail to adequately capture the complexity of real-world attributes. As a solution, we investigate a novel Diffusion-based Guided Anomaly Imputation Model to generate realistic anomalies which are then evaluated based on its impact on anomaly detection performance (using a novel Residual-Spectral Diffusion Model). We focus on 7 anomalies (StepChange, MultiStepChange, Mirror, Repeating, StuckMAX, StuckMIN, and PowerCycling) across 14 NILM (Non-Intrusive Load Monitoring) datasets: REFIT (Houses - 1, 2, 3, 5, 7, 9, 15), UKDALE (Houses - 1, 2, 5), AMPds2 (House - 1), GREEND (Houses - 0, 1, 3). The results show that diffusion imputation does not degrade overall detectability and the relative ordering of anomaly difficulty is, for the most part, preserved. The distribution analysis shows that diffusion anomalies, generally, overlap with normal behaviour. Diffusion Imputation reshapes anomalies rather than inserting trivial or noisy characteristics, thus, producing context-aware anomalies appropriate for evaluation. In conclusions, our proposed model provides a realistic framework for benchmarking anomaly detection methods in Smart Meters.

EXPLANATION OF FILES

1. DatasetCreation.ipynb: <br>
  a. From datasets (7xREFIT/3xUKDALE/3xGREEND/1xAMPds2) and appliances (Fridge/Dishwasher/WashingMachine), creates files with 15-minute frequency. <br>
  b. Creates the Centroids file (average active_power for Fridge/Dishwasher/WashingMachine/Nothing). <br>
  c. Creates the 7 anomalies (StepChange, MultiStepChange, Mirror, Repeating, StuckMAX, StuckMIN, and PowerCycling) for 7 days. <br>
  d. Merges normal and anomalies together while specifying ground_truth_anomaly and ground_truth_appliance. <br>

2. TimeSeries_AnomalyDetection.ipynb

3. TimeSeries_AnomalyImputation.ipynb
