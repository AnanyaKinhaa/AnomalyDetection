# Anomaly Detection in Financial Transactions
### Barclays Hack-O-Hire Hackathon 1st Position Project Repo

## Introduction
 - Our Anomaly Detection System distinguishes itself through advanced machine
learning algorithms and real-time processing capabilities. By employing
 Python for its robust libraries and AWS services for its seamless integration,
 database management systems, ETL, and processing, our system ensures a high
 detection rate of anomalous transactions with minimal false positives. This
 combination of technologies allows for the agile development of a scalable,
 secure, and efficient anomaly detection platform.

 - One of the unique aspects of the ADS is its emphasis on data security and
 privacy. Recognizing the sensitivity of financial data, the system incorporates
 end-to-end encryption, leveraging AWS KMS for key management and ensuring
 that all data in transit and at rest is securely encrypted. Access controls and
 regular audits further enhance the system's security posture, safeguarding
 against unauthorized access and data breaches. Our Anomaly Detection System,
 augmented by Tableau's visualization capabilities, marks a significant
 advancement in any organization's ability to identify and mitigate fraud
 effectively

 ## Problem Statement
 The challenge is to efficiently identify and rectify irregularities and
 anomalous activities in real time, ensuring the integrity and reliability of the
 financial transaction process.

 ## Tech Stack
 - The project utilizes a blend of technologies to build the anomaly detection system. 
Python serves as the backbone for data manipulation and analysis, leveraging libraries like
 pandas and scikit-learn. 
- Data is stored securely in AWS S3 and RDS, where S3 talks with the model directly and RDS
 stores the data in tabular form. 
- AWS Glue streamlines data extraction and transformation. 
- Machine learning tools play an important role, with SageMaker offering a platform for training
 and deploying custom models if needed. Anomaly detection logic is primarily implemented in
 Python, with results stored in S3. 
- Additionally, AWS CloudWatch monitors key metrics for performance insights. Visualization
 tools like Tableau can be integrated for further data exploration. 
- Security is a priority, with AWS Key Management Service (KMS) safeguarding data throughout
 the process

![image](https://github.com/AnanyaKinhaa/AnomalyDetection/assets/96624771/ec278850-476c-43e8-8467-97d2e01184bc)

## Implementation
We'll transfer the data to the anomaly
 detection module which uses Python
 libraries like PyTorch and Scikit Learn, and
 automate the process with AWS Step
 Functions. 
 
![image](https://github.com/AnanyaKinhaa/AnomalyDetection/assets/96624771/9b51d49d-a805-4b6a-997f-ed4acbb6ac5b)

Model:
 1. Isolation Forest:
 - Concept: This algorithm isolates
 instances deviating significantly from
 the expected data pattern.
 - Implementation: Train the model on
 the table. New transactions are
 scored based on isolation level, with
 higher scores indicating higher
 likelihood of anomalies

 2. Local Outlier Factor (LOF):
 - Concept: Identifies anomalies by
 comparing a data point's local
 density deviation to neighbors.
 - Implementation: Train LOF on
 enriched transaction data, assigning
 new transactions outlier factor
 scores. Higher scores imply higher
 outlier likelihood.
 3. LSTMs (Long Short-Term Memory):
 - Concept: 
RNN type learning
 sequential patterns, suitable for
 analyzing transaction time series.
 - Implementation: Train LSTM on
 historical transaction sequences per
 client/account. New transactions
 predict subsequent behavior, with
 deviations signaling anomalies

Detectable Anomalies:
 - Unusual 
spending 
sequences
 deviating from the client's typical
 transaction patterns.
- Transactions occurring outside the
 client's typical spending hours or
 locations
-Transactions exceeding the client's
 usual daily or monthly spending
 limits.
- Sudden bursts of transactions or
 transactions 
occurring 
geographically unusual locations.
  





 
