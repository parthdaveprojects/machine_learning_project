# Predictive Maintenance for Industrial Machines

## 📌 Project Overview
This project focuses on building a **predictive maintenance system** using machine learning techniques to prevent unexpected industrial machine failures. The system predicts different types of machine failures in advance, enabling proactive maintenance, reducing downtime, and lowering operational costs.

This was developed as a **Capstone Project**  by **Parth Bhagyesh Dave** using IBM Watsonx AutoAI and IBM Cloud Services.

---

## Outline
- Problem Statement
- Proposed Solution
- System Developmen Approach
- Algorithm & Deployment
- Result
- Conclusion
- Future Scope
- References

---

## 🚨 Problem Statement

In modern industries, unexpected machinery failures can lead to costly downtime and delays. To address this, the aim is to develop a predictive maintenance model that can anticipate failures before they happen. By analysing sensor data from machines, the model will learn to detect patterns that typically occur before a failure. The focus is on creating a multiclass classification system capable of predicting specific failure types such as:

Tool wear failure
Heat dissipation failure
Power failure
Random failures
Overstrain failures

This solution empowers industries to perform maintenance proactively, reducing unexpected breakdowns, downtime, and overall operational costs.


---

## ✅ Proposed Solution

In response to unplanned equipment failures, our solution involves developing a predictive maintenance model powered by sensor data and machine learning.

**Data Collection:**
- Acquired historical sensor data from industrial machines.
- Dataset includes operational metrics and labeled failure types.
- Covers variables like temperature, torque, speed, and tool wear.

**Data Preprocessing:**
- Manual Step: Dropped non-informative column UDI
- Automated Steps via IBM AutoAI:
    - Handled missing values (if any)
    - Encoded categorical variable (Type)
    - Scaled and normalized numerical features
    - Split data into training and testing sets
    - Selected suitable transformations for model compatibility

**Machine Learning Algorithm:**
- IBM AutoAI selected 3 algorithms as per data and select multiple models and   create pipelines.
- Top Models Selected:
    1. Snap Random Forest Classifier
    2. Random Forest Classifier
    3. Snap Decision Tree Classifier
- Models were compared based on:
    1. Prediction Accuracy
    2. Training and Inference Time

**Deployment**
- Best model deployed using IBM Cloud AutoAI platform.
- Deployment considerations:
    1. High Accuracy
- Deployed as a REST API endpoint.
- Model accessibility: Python, Javascript, Java, Scala and cURL

**Evaluation:**
- Model performance was assessed using metrics like accuracy and confusion matrix.
- Evaluation considered:
    1. Model precision
    2. Class-wise prediction performance
    3. Deployment response time
- Snap Random Forest Classifier achieved 99.5% accuracy.

## 🧠 Tech Stack
- **Platform**: IBM Cloud
- **Libraries**:
  - `requests` (for REST API)
- **Tools**:
    1. IBM Watsonx.ai,
    2. Jupyter Notebook
    3. IBM AutoAI,
    4. IBM Cloud Object Storage,
    5. IBM Watsonx.ai Runtime

## Alogrithm & Deployment

**Algorithm Selection**
- IBM AutoAI automatically explored various machine learning pipelines. It shortlisted three high-performing algorithms:
    1. Snap Random Forest Classifier (Best Performer)
    2. Random Forest Classifier
    3. Snap Decision Tree Classifier
  - Snap Random Forest was chosen due to its high accuracy (99.5%) and ability to handle complex classification tasks effectively.

 **Data Input:**
- The model utilized features such as:
    1. Air temperature [K]
    2. Process temperature [K]
    3. Rotational speed [rpm]
    4. Torque [Nm]
    5. Tool wear [min]
    6. Machine type and product ID (encoded)
    7. The target variable was the Failure Type (e.g., Tool Wear, Heat Dissipation, etc.).

**Training Process:**
- Model training was handled by IBM AutoAI
- AutoAI performed automatic feature engineering and hyperparameter optimization (HPO-1, HPO-2)
- Dataset split for training and validation internally by AutoAI pipelines

**Prediction Process:**
- The trained model predicts the failure type based on sensor input
- Model supports batch and real-time prediction through deployed API
- Prediction confidence scores (probabilities) are also provided

## Conclusion

- Successfully developed a predictive maintenance model using real-time sensor data to anticipate industrial machine failures.
- Leveraged IBM AutoAI for automated data preprocessing, algorithm selection, and model optimization.
- Snap Random Forest Classifier achieved an impressive 99.5% accuracy, making it the ideal choice for deployment.
- The system enables proactive maintenance, minimizing downtime, reducing operational costs, and improving machine reliability.
- Deployed model is accessible through multiple platforms (Python, Java, JavaScript, cURL), ensuring easy integration into existing systems.

## Future Scope

- **Integration of More Sensor Types:** Extend the current dataset by integrating additional machine sensors (e.g., vibration, acoustic, or thermal imaging) for richer insights and improved failure prediction.
- **Model Generalization:** Adapt the trained model to work across different types of industrial machines and environments to ensure scalability and robustness.
- **Real-Time Edge Deployment:** Implement the model on edge devices directly connected to machines for real-time monitoring and faster response to anomalies.
- **Automated Retraining Pipelines:** Set up an automated feedback loop where new operational data helps in continuous retraining and refinement of the model.
- **Cost-Aware Maintenance Scheduling:** Enhance the system to not only predict failures but also recommend cost-optimized maintenance schedules based on operational hours and failure severity.
- **Wider Platform Integration:** Expand model usability by integrating with industrial platforms like PLCs, SCADA systems, or cloud-based monitoring dashboards for seamless operations.

## References

- Dataset:
-     https://www.kaggle.com/datasets/shivamb/machine-predictive-maintenance-classification
- IBM Cloud Dashboard:
-     https://cloud.ibm.com/login
- IBM watsonx.ai Studio:
-     https://cloud.ibm.com/services/data-science-experience/crn%3Av1%3Abluemix%3Apublic%3Adata-science-experience%3Aau-syd%3Aa%2Faab9312cccf3498ca3d3f656bf4e348d%3A04329999-f229-40fd-9edb-b53031652aa5%3A%3A?paneId=manage
- Watson Studio learning path:
-     https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/quickstart-tutorials.html?context=wx
- Documentation for Cloud Pak for Data as a Service:
-     https://au-syd.dai.cloud.ibm.com/docs/content/wsj/getting-started/welcome-main.html?context=cpdaas&audience=wdp
- Documentation for IBM watsonx as a Service:
-     https://au-syd.dai.cloud.ibm.com/docs/content/wsj/getting-started/welcome-main.html?context=wx&audience=wdp
