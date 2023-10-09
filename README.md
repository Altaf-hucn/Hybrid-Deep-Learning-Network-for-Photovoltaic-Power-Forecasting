[Hybrid-Deep-Learning-Network-for-Photovoltaic-Power-Forecasting](https://www.hindawi.com/journals/complexity/2022/7040601/)


## Abstract
For efficient energy distribution, microgrids (MG) provide significant assistance to main grids and act as a bridge between the power generation and consumption. Renewable energy generation resources, particularly photovoltaics (PVs), are considered as a clean source of energy but are highly complex, volatile, and intermittent in nature making their forecasting challenging. Thus, a reliable, optimized, and a robust forecasting method deployed at MG objectifies these challenges by providing accurate renewable energy production forecasting and establishing a precise power generation and consumption matching at MG. Furthermore, it ensures effective planning, operation, and acquisition from the main grid in the case of superior or inferior amounts of energy, respectively. Therefore, in this work, we develop an end-to-end hybrid network for automatic PV power forecasting, comprising three basic steps. Firstly, data preprocessing is performed to normalize, remove the outliers, and deal with the missing values prominently. Next, the temporal features are extracted using deep sequential modelling schemes, followed by the extraction of spatial features via convolutional neural networks. These features are then fed to fully connected layers for optimal PV power forecasting. In the third step, the proposed model is evaluated on publicly available PV power generation datasets, where its performance reveals lower error rates when compared to state-of-the-art methods.
## Proposed Framework 
![Image 1 Description](Results/Framework.png)

## Details About  Datasets

| Dataset                   | Technical Specification          | Value                   |
|---------------------------|----------------------------------|-------------------------|
| DKASC-AS-1A               | Manufacturer: Trina             | PV Technology: mono-Si  |
|                           | Array Structure: Dual Axis Tracker | Panel Size: 2 x 38.37 m² |
|                           | Array Tilt/Azimuth: Variable, Dual axis tracking | Generation Capacity of a Panel: 175W |
|                           | Number of Solar Panels: 2×30    | Power Generation Capacity: 10.5kW |
|                           | Duration: 08-14-2013 ~ 07-01-2021 |                          |
| DKASC-AS-1B               | Manufacturer: Trina             | PV Technology: mono-Si  |
|                           | Array Structure: Dual Axis Tracker | Panel Size: 4 x 38.37 m² |
|                           | Array Tilt/Azimuth: Variable, Dual axis tracking | Generation Capacity of a Panel: 195W |
|                           | Number of Solar Panels: 4 × 30   | Power Generation Capacity: 23.4kW |
|                           | Duration: 8-14-2013 ~ 7-1-2021   |                          |
| DKASC-AS-2Eco             | Manufacturer: eco-Kinetics      | PV Technology: mono-Si  |
|                           | Array Structure: Dual Axis Tracker | Panel Size: 199.16 m²   |
|                           | Array Tilt/Azimuth: Fixed, Tilt = 20', Azimuth = 0' | Generation Capacity of a Panel: 170W |
|                           | Number of Solar Panels: 156      | Power Generation Capacity: 26.52kW |
|                           | Duration: 8-24-2010 ~ 8-22-2020  |                          |
| DKASC-Yulara-SITE-3A      | PV Technology: mono-Si          | Array Structure: Roof Mount |
|                           | Panel Type: SunPower SPR-327NE   | Array Tilt/Azimuth: Tilt = 10, Azi = 0 (Solar North) |
|                           | Generation Capacity of a Panel: 327W | Number of Solar Panels: 69 |
|                           | Power Generation Capacity: 22.56kW | Duration: 4-1-2016 ~ 6-27-2022 |

## Access to Our Dataset

Hello there! :wave:

Thank you for your interest in our datasets. Due to size limitations on GitHub, we haven't uploaded the entire dataset directly. 
:email: If you wish to access or use our datasets, please send a request to the following email, and we'll provide you with further instructions:
**altafh3797@gmail.com**
We appreciate your understanding and patience. Looking forward to assisting you!

## Results
# Model Performance on Datasets

| Dataset             | Model         | RMSE  | MSE    | MAE    | MBE     |
|---------------------|---------------|-------|--------|--------|---------|
| DKASC-AS-1A [67]    | Decision Tree | 0.4531| 0.2053 | 0.2484 | 0.0684  |
|                     | SVR           | 0.4309| 0.1857 | 0.2373 | 0.0463  |
|                     | LSTM          | 0.3118| 0.0972 | 0.1578 | -0.0283 |
|                     | GRU           | 0.3004| 0.0902 | 0.144  | 0.0322  |
|                     | CNN-LSTM      | 0.2873| 0.0825 | 0.117  | -0.0054 |
|                     | CNN-GRU       | 0.2606| 0.0679 | 0.1535 | 0.082   |
|                     | LSTM-CNN      | 0.2239| 0.0501 | 0.1485 | -0.1472 |
|                     | GRU-CNN       | 0.1468| 0.0216 | 0.0742 | 0.0171  |
| DKASC-AS-1B [68]    | Decision Tree | 0.5344| 0.2856 | 0.3365 | -0.0824 |
|                     | SVR           | 0.5087| 0.2588 | 0.303  | 0.0709  |
|                     | LSTM          | 0.3949| 0.1559 | 0.2219 | 0.0287  |
|                     | GRU           | 0.389 | 0.1514 | 0.2064 | 0.0089  |
|                     | CNN-LSTM      | 0.2776| 0.0771 | 0.1531 | 0.0172  |
|                     | CNN-GRU       | 0.262 | 0.0686 | 0.1364 | -0.0318 |
|                     | LSTM-CNN      | 0.2496| 0.0623 | 0.208  | -0.187  |
|                     | GRU-CNN       | 0.1727| 0.0298 | 0.0923 | 0.0235  |
| DKASC-AS-2Eco [69]  | Decision Tree | 0.4911| 0.2412 | 0.1909 | 0.0709  |
|                     | SVR           | 0.456 | 0.2079 | 0.2246 | 0.0187  |
|                     | LSTM          | 0.3167| 0.1003 | 0.157  | -0.0158 |
|                     | GRU           | 0.3302| 0.109  | 0.1726 | -0.0176 |
|                     | CNN-LSTM      | 0.2959| 0.0876 | 0.1449 | -0.0143 |
|                     | CNN-GRU       | 0.2801| 0.0784 | 0.1467 | 0.0132  |
|                     | LSTM-CNN      | 0.2274| 0.0517 | 0.1599 | -0.0155 |
|                     | GRU-CNN       | 0.1646| 0.0271 | 0.1157 | -0.0641 |
| DKASC-Yulara-SITE-3A [70] | Decision Tree | 0.416 | 0.173  | 0.2566 | 0.0159  |
|                     | SVR           | 0.4966| 0.2466 | 0.2443 | -0.0122 |
|                     | LSTM          | 0.3627| 0.1315 | 0.1735 | 0.0561  |
|                     | GRU           | 0.3864| 0.1493 | 0.2368 | -0.0013 |
|                     | CNN-LSTM      | 0.3056| 0.0934 | 0.1388 | -0.0153 |
|                     | CNN-GRU       | 0.3063| 0.0938 | 0.1506 | 0.0354  |
|                     | LSTM-CNN      | 0.2465| 0.0608 | 0.155  | 0.0919  |
|                     | GRU-CNN       | 0.1715| 0.0294 | 0.1126 | 0.0099  |



