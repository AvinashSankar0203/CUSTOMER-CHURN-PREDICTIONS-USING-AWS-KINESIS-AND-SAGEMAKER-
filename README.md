# 🚀 Real-Time Customer Churn Prediction using AWS Kinesis & SageMaker

An end-to-end **cloud-native machine learning pipeline** that ingests streaming customer data, performs distributed feature engineering, and trains a churn prediction model using AWS managed services.

This project demonstrates **Data Engineering + Machine Learning + MLOps** in a production-style architecture.

---

## 📌 Project Highlights

✅ Real-time data ingestion with Kinesis  
✅ Distributed preprocessing using PySpark (EMR)  
✅ End-to-end AWS ML workflow  
✅ Correlation-driven feature engineering  
✅ Role-based IAM access (enterprise-style security)  
✅ Production-oriented architecture  

---

## 🏗️ Architecture

### 🔄 Pipeline Flow


This architecture enables **real-time ML training from streaming data**, similar to modern subscription and fintech platforms.

---

## 🧰 Tech Stack

| Layer | Technology |
|-------|------------|
Data Ingestion | AWS Kinesis Data Streams |
Stream Delivery | AWS Kinesis Firehose |
Storage | Amazon S3 |
Distributed Processing | AWS EMR + PySpark |
ML Platform | Amazon SageMaker |
Automation | AWS CLI |
Security | AWS IAM Roles |

---

## 📊 Dataset

**Telco Customer Churn Dataset**

- 7,000+ customers
- 21 features
- Target variable: `Churn`

### Example Features:

- Tenure  
- Contract type  
- Payment method  
- Monthly charges  
- Internet service  

---

## ⚙️ Data Engineering & Feature Processing

✔ Removed customer identifiers to avoid model bias  
✔ Handled missing & inconsistent records  
✔ Filtered invalid tenure values  
✔ Encoded categorical variables  
✔ Correlation-based feature selection  
✔ Normalized numerical features  

All transformations were executed using **PySpark inside SageMaker Data Wrangler**.

---

## 🤖 Model Development

**SageMaker Quick Build – Classification**

- Training time: ~10 minutes

### 📈 Performance

| Metric | Score |
|--------|-------|
Accuracy | **76.26%** |
F1 Score | **0.642** |

> Note: The goal of this project was to design a **scalable real-time ML pipeline**, not hyperparameter tuning.

---

## 🔐 IAM & Enterprise Design

Implemented a custom **Data Scientist IAM role**:

### Allowed Access:
- EMR
- S3
- Kinesis
- SageMaker

### Restricted Access:
- All other AWS services

This mirrors **real-world organizational cloud governance**.

---

## 💼 Business Impact

This system enables companies to:

- Predict churn from streaming behavioral data
- Trigger real-time retention strategies
- Continuously retrain models on fresh data
- Build scalable ML infrastructure without managing servers

---

## 📷 Architecture & Workflow

Detailed implementation, screenshots, and system design are available in the project report:

📄 **Project Documentation:**  
Customer Churn Prediction using AWS Kinesis and SageMaker

---

## 🔮 Future Improvements

- Real-time inference endpoint deployment
- AWS Lambda automation for fully serverless pipeline
- Hyperparameter tuning
- CI/CD for ML workflows
- Advanced feature engineering

---

## 🧪 How to Reproduce

### 1️⃣ Configure AWS CLI


### 2️⃣ Create Required Resources

- S3 bucket
- Kinesis Data Stream
- Firehose delivery stream
- EMR cluster
- SageMaker Studio

### 3️⃣ Simulate Streaming Data

Send JSON records from local machine to Kinesis at time intervals.

### 4️⃣ Run EMR PySpark Job

Aggregate chunked data → single training dataset.

### 5️⃣ Train Model in SageMaker

Use Data Wrangler → Quick Build.

---

## 📚 Key Learnings

- Designing real-time ML systems
- Distributed feature engineering with Spark
- Production-style IAM implementation
- Cloud-native MLOps workflow
- Data lake architecture on AWS

---

## 👥 Contributors

- Ali Guzelyel  
- **Avinash Sankar**  
- H. V. Veerakkumaar  
- Taufeeq A. Mohammed  

---
