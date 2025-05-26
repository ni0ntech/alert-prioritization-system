# 🛡️ Cloud Sentinel: Anomaly Detection in AWS Logs with Machine Learning

Cloud Sentinel is a fully serverless security monitoring solution that leverages AWS infrastructure and Python-powered machine learning to detect anomalous behavior in real-time from CloudTrail logs. Designed for threat hunters, SOC analysts, and cloud security professionals, this project showcases the fusion of automation, ML, and cloud-native architecture to catch suspicious actions before they escalate.

## 🚀 Project Goals

- Ingest and process CloudTrail logs in real-time
- Train a machine learning model to detect anomalies in AWS account activity
- Automate detection, alerting, and logging of anomalous events using serverless AWS services

---

## 🏗️ Architecture

```
User Activity → CloudTrail → S3 Bucket
                             ↓
                      EventBridge Trigger
                             ↓
                      Lambda Function
            (Preprocess Logs + Feature Extraction)
                             ↓
                    SageMaker ML Model
                             ↓
               Classification & Alert via SNS
```

---

## 🔧 Technologies Used

- **AWS CloudTrail** – Collect account activity
- **AWS S3** – Store log data
- **AWS Lambda** – Python-based processing
- **Amazon EventBridge** – Trigger processing pipelines
- **Amazon SageMaker** – Train & deploy ML models
- **Amazon SNS** – Push alerts
- **Python (boto3, pandas, scikit-learn)** – Data engineering & model development

---

## 🧠 Machine Learning Approach

An **Isolation Forest** model is trained on historical CloudTrail logs to detect outliers in user behavior. Features include event names, IP addresses, user types, geolocation (optional), and time-based patterns.

Bonus: a comparative autoencoder neural network may be used for evaluation in SageMaker notebooks.

---

## 📁 Project Structure

```
cloud-sentinel/
├── lambda/               # Serverless functions
├── model/                # ML training and evaluation
├── s3/                   # Sample log data
├── cloudformation/       # Infra-as-code (optional)
├── cli_tool/             # Optional CLI for manual analysis
└── README.md
```

---

## 📊 Future Enhancements

- GeoIP enrichment
- IAM-based user profiling
- Integration with QuickSight for dashboards
- Retraining pipeline based on log volume or time windows

---

## 🧑‍💻 Ideal For

- Security Operations Center (SOC) portfolios
- Demonstrating cloud-native detection engineering
- Hands-on AWS and machine learning experience
- Showcasing Python automation in a real-world infosec use case

---

## 📸 Screenshots & Demo

Coming soon...

---

## 🔐 Author

**Joshua Rubio**
InfoSec Specialist | Cloud Security | Threat Hunter | AI Integrator  
[ni0ntech.com](https://www.ni0ntech.com)
