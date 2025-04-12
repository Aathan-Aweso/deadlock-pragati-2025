# Team Deadlock- Pragati AI Hackathon 2025

## **Project Overview**
This project addresses critical healthcare challenges in rural India, including inadequate access to medical information, doctor shortages, language barriers, disconnected patient records, and underutilized government healthcare schemes. The solution is a comprehensive AI-powered platform that connects patients, doctors, and ASHA workers through a unified system. It provides multilingual support for booking appointments, managing patient records, preliminary disease diagnosis, personalized healthcare guidance, and identifying eligible government healthcare schemes. The platform is designed to function effectively in low-resource settings with limited internet connectivity.

---

## **Key Features**

![image](https://github.com/user-attachments/assets/9fe9bdfc-a323-4ba2-9a7b-50177839052d)

1. **Multilingual Support**: Enables users to interact with the platform in their preferred regional language.
2. **Medical Report Generation**: Structured medical reports based on symptoms, consultations, and test results.
3. **IVRS Appointment Booking**: Interactive Voice Response System for automated appointment reminders.
4. **Online Consultation**: Facilitates virtual doctor consultations.
5. **Appointment Scheduling**: Easy booking of doctor appointments.
6. **Time Series Forecasting**: Predicts future drug supply needs using historical data to prevent stockouts.
7. **Personalized Dietary Recommendations**: AI-driven nutrition guidance verified by dietitians.
8. **Healthcare Scheme Awareness**: Simplifies access to government health schemes using patient data analysis.
9. **High-Risk Pregnancy Detection**: Early identification and notification for timely interventions.

---

## **Solution Architecture**

![Booking drawio (5)](https://github.com/user-attachments/assets/c4880849-4de2-4c35-a8ab-f826d2926a9a)


### **1. User Interaction Layer**
- Users interact via mobile phones using an IVR system powered by Amazon Connect.
- Amazon Lex handles conversational AI queries with multilingual support via Bhashini API for translation.

### **2. Processing Layer**
- AWS Lambda functions process intents such as booking appointments or retrieving scheme eligibility.
- Amazon API Gateway acts as the public endpoint for Lambda functions.

### **3. Application Backend**
- Built with Python and Node.js using Langchain and Langflow for conversational workflows.
- Hybrid search (BM25 + BGE-M3 embeddings) implemented using FAISS vector store.

### **4. Data Layer**
- DynamoDB stores patient records, appointments, and medical data.
- FAISS vector store manages embeddings of medical documents and guidelines.

### **5. Deployment**
- Hosted on AWS Amplify with user authentication managed by AWS Cognito.
- Llama3.3-70b LLM inference powered by Cerebras for high-speed processing.

---

## **Open-Source Technologies Used**
### **Frontend**
- React.js
- Tailwind CSS

### **Backend**
- Python and Node.js
- Langchain and Langflow
- FAISS (Vector Database)
- AWS DynamoDB (Database)
- Bhashini API (Voice Translation)
- Llama3.3-70b (LLM)
- BGE-M3 (Embedding Model)
- Meta Prophet (Time Series Forecasting)

### **Cloud Services**
- AWS Lambda
- AWS API Gateway
- Amazon Connect
- Amazon Lex
- Amazon Pinpoint
- AWS Cognito
- AWS Amplify

---

## **Scalability**
The solution leverages AWS services like Lambda, DynamoDB Auto Scaling, and Amazon Lex for seamless scalability:
1. AWS Lambda scales automatically to handle up to 10,000 requests per second per region.
2. DynamoDB supports horizontal scaling for handling millions of requests daily.
3. Amazon Lex processes large volumes of conversational queries efficiently.

---

## **Datasets Used**

The solution uses a synthetic dataset generated with [mostly.ai](https://mostly.ai/):
- Weekly drug sales data from 2020–2025 across five regions in India.
---

## **Addressing Connectivity Challenges**
The platform is cloud-based but optimized for low-resource settings:
1. Supports low-bandwidth environments through lightweight interfaces and voice-based interactions.
2. Cost-effective cloud computation is enabled via Cerebras' high-performance inference services.

---

## **Intended Impact**
The solution aims to:
1. Improve health literacy in underserved communities.
2. Reduce delays in diagnosis and treatment.
3. Enhance access to government healthcare schemes.
4. Focus on maternal health, child nutrition, and overall healthcare accessibility.

By leveraging AI-driven personalization, multilingual support, and scalable architecture, this solution empowers rural communities with accessible and efficient healthcare services.

## **Folder Structure**

```
📦 
├─ README.md
└─ ivr
   ├─ .gitignore
   ├─ README.md
   ├─ package-lock.json
   ├─ package.json
   ├─ public
   │  ├─ favicon.ico
   │  ├─ index.html
   │  ├─ logo192.png
   │  ├─ logo512.png
   │  ├─ manifest.json
   │  └─ robots.txt
   └─ src
      ├─ App.css
      ├─ App.js
      ├─ App.test.js
      ├─ index.css
      ├─ index.js
      ├─ logo.svg
      ├─ reportWebVitals.js
      └─ setupTests.js
```

## Authors

- [Deepu John](https://github.com/deepu-RW)
- [Aathan](https://github.com/Aathan-Aweso)
- [Riddhishwar S](https://github.com/deepu-RW)

