Data-Beans Project Learning Guide (learn.md)
Welcome to the Data-Beans project! This guide is designed to help you understand the project's purpose, the technologies used, and how you can get the most out of it.

🎯 What You Will Learn with This Project
This demo project shows you how modern data and AI technologies can be applied in practical business scenarios. By completing this project, you will gain proficiency in the following areas:

Generative AI (GenAI) Applications: You will learn to generate synthetic data such as text, images, and audio using Large Language Models (LLMs) like Google's Gemini, and to create business-oriented insights.

Data Analysis on Google Cloud: You will see how to store, query, and integrate large datasets with GenAI services using cloud-based data warehouses like BigQuery.

End-to-End Solution Architecture: You will experience the entire lifecycle of a project, from data generation and analysis to insight extraction and marketing campaign creation.

Serverless and Managed Tools: You will discover the advantages of focusing directly on data science and AI tasks instead of infrastructure management by working in managed notebook environments like Colab Enterprise.

Infrastructure as Code (IaC): You will learn how to automatically provision and configure the entire Google Cloud infrastructure using Terraform and shell scripts.

Vector Databases and RAG: You will learn to convert text data like customer reviews into vectors to perform semantic searches and implement the RAG (Retrieval-Augmented Generation) pattern.

🛠️ Technologies Used
This project utilizes the following core technologies and services:

Google Cloud Platform (GCP):

BigQuery: Serverless data warehouse for data storage and analysis.

Vertex AI: AI platform for accessing Gemini models, Colab Enterprise Runtimes, and generating images and audio.

Google Cloud Storage: For storing generated files (images, audio, etc.).

Compute Engine: Virtual machine for running the deployment scripts.

Generative AI (GenAI):

Gemini Models: For generating text-based insights, synthetic data, and marketing copy.

Imagen: For generating images from text descriptions.

Text-to-Speech API: For generating audio files from text.

Infrastructure and Automation:

Terraform: For creating and managing Google Cloud resources with code.

Shell Scripts (.sh): For automating the deployment process.

Git & GitHub: For version control and code repository.

Data Science and Development:

Colab Enterprise Notebooks: For interactively running analysis and AI steps.

Python: The main programming language in the notebooks.

📂 Project Structure and Modules
The project consists of various modules aimed at improving the business processes of "Data Beans," a fictional coffee truck company. Each module contains Colab notebooks focused on a specific business scenario:

Marketing Campaign: Generates insights and copy for an effective marketing campaign based on existing data.

Weather and Event Analysis: Analyzes external factors that could affect sales (weather, local events) and extracts insights from this data.

Menu A/B Testing: Creates new menu items and designs a marketing campaign for them.

Customer Reviews Analysis:

Synthetic Data Generation: Generates realistic customer reviews, images, and audio files.

Analysis and Theme Detection: Identifies the main themes in the reviews (e.g., "coffee quality," "service speed").

Automated Responses and Action Plans: Suggests custom responses to reviews and actions for the company to take (e.g., "Apologize to the customer").

Advanced Search with RAG: Converts customer reviews into vectors to enable semantic search for common issues.

🚀 Setup and Getting Started
Follow the steps below to set up the project in your own Google Cloud environment.

1. Prerequisites
Before you begin the installation, ensure the following tools are installed on your local machine or the VM you will be using:

Git

Google Cloud CLI (gcloud)

Terraform

jq

2. Clone the Project
Download the project files to your machine:

Bash

git clone https://github.com/GoogleCloudPlatform/data-beans
cd data-beans
3. Log in to Google Cloud
Log in to your Google account with the gcloud CLI:

Bash

gcloud auth login
gcloud auth application-default login
4. Start the Deployment
The project can be deployed in two different ways, depending on your Google Cloud permissions:

Option A: With Elevated Privileges (Org Level)

This is the simplest method. By running the following script, a new project will be created for you, and all resources will be deployed automatically.

Bash

source deploy.sh
Option B: On an Existing Project (Project Owner)

Use this option if you have a pre-existing project and you have the "Owner" role in it.

Open the deploy-use-existing-project-non-org-admin.sh file with a text editor.

Update the variables inside the file, such as the project ID, with your own project information.

Run the updated script:

Bash

source deploy-use-existing-project-non-org-admin.sh
Important Note: Deployment via Cloud Shell is not currently supported. Please use your local machine or a Compute Engine virtual machine.

🔬 Running and Exploring the Notebooks
After the deployment is complete, navigate to Vertex AI > Colab Enterprise > Runtimes in the Google Cloud Console. Find the colab-enterprise-runtime and start running the notebooks.

Pay Attention to the Order: Some notebooks require data generated by another notebook to run. For example, you must run the steps in the Customer Reviews module in the specified order (first data generation, then theme detection, etc.). The "How to Run the Notebooks" section in the README.md file will show you the correct sequence.

Cost Control: To minimize costs when you are not actively using the project, you can delete the Colab Enterprise Runtime. You can easily recreate it from the template when you want to use it again.

You are now ready to explore the Data-Beans project and learn about the power of GenAI in the business world!
