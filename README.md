# Hard-Disk-Drive-Failure-Detection
The task is to predict the failed Hard Disk Drive of different vendors.

## Description:
It is the Binary class classification problem where we have to predict Hard Drive failure. These are predicted by using attributes that are recorded during normal operations of hard drive. These attributes are known as SMART(Self – Monitoring and Reporting Technology) which is the monitoring system included in computer HDD. The motive of this prediction is to reduce the rate of failures as a cost saving measure by the HDD vendors and software running on the host system may notify the user so preventive action can be taken to prevent data loss and failing drive can be replaced and data integrity is maintained. The HDD is said to be failed or critical when some of these attributes crosses the threshold values. Depending upon the manufacturers they use different SMART attributes in which the common attributes are like Read Error Rate, Throughput Performance, Spin-Up Time etc.

### Dataset link : https://www.backblaze.com/b2/hard-drive-test-data.html#how-you-can-use-the-data .

Since HDD are from different vendors several attributes will vary from each vendors. Thus, after EDA only most common features are found and used for the analysis. The main problem with this is high imbalance data where resampling techniques of oversampling the minority class with SMOTE and undersampling the majority class is applied. Feature Engineering techinques like response encoding and mathematical transformation were incorporated. 

### Features of Data:
Date – The date of the file in yyyy-mm-dd format.

Serial Number – The manufacturer-assigned serial number of the drive.

Model – The manufacturer-assigned model number of the drive.

Capacity – The drive capacity in bytes.

Failure – Contains a “0” if the drive is OK. Contains a “1” if the drive is failed.

S.M.A.R.T Attributes - Raw and Normalized.

## Performance Metrics:
Confusion Matrix, AUC Score, ROC-AUC Curve

## Summary

|  Data|Model| ROC-Score |
|------|----|----------------------|
|      Val |Logistic Reg| 0.9392 |
|     | SVC|  0.9357 |
|      |Stacking|  0.9420 |
|      |GBDT| 0.8993 |


|  Data|Model| ROC-Score |
|------|----|----------------------|
|      Test |Logistic Reg| 0.8468 |
|     | SVC|  0.9203 |
|      |Stacking|  0.9136 |
|      |GBDT| 0.8946 |

With this approach Kernel SVC and Stacking classifier gives AUC score of 0.9203 and 0.9136 on Test Data.

### Blog link: https://harishkumar-69065.medium.com/hdd-failure-detection-4a4797fae7e

## Contains 1 file:
HDD_Failure_Detection.ipynb - EDA, Feature pre-processing and Modelling
