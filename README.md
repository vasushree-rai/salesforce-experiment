
# Salesforce Apex Email Service Component

A robust, production-ready Salesforce Apex utility class designed to handle email automation. This component supports sending transactional single HTML/Text emails and automates personalized communication utilizing Salesforce Email Templates.

## 🚀 Features

*   **Single Email Utility**: Quickly send manual HTML or plain text emails to single or multiple recipients.
*   **Template Integration**: Seamlessly fetch and distribute native Salesforce Email Templates while automatically merging context fields (`TargetObjectId` and `WhatId`).
*   **Bulk-Ready Design**: Structured with collections (`List<Messaging.Email>`) to optimize system governance and adhere to Apex transaction limits.
*   **Logging Controls**: Built-in verification loop inspecting `Messaging.SendEmailResult` for instantaneous debug logs.

## 📸 Proof of Concept

Below is a snapshot demonstrating successful execution and delivery verification 
#sending a mail using salesforce and showing an exec log
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/1f674261-3d19-4eaf-833a-11a48d3b1534" />

<img width="992" height="611" alt="image" src="https://github.com/user-attachments/assets/ec6e5617-5e6f-4ad3-8354-9d6c9d3bde2d" />

## 📋 How to Deploy & Test

### Prerequisites
Before running execution tests, ensure your Salesforce Organization permits outbound email transmissions:
1. Navigate to **Setup** -> **Deliverability**.
2. Set the **Access Level** dropdown option to **All Email** and click **Save**.
   
