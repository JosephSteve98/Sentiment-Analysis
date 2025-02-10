# Sentiment-Analysis
SENTIMENT ANALYSIS Model - Deploy using AWS Services  or Hugging Face

# Introduction
This project focuses on deploying a Sentiment Analysis Model using AWS services and making it accessible through a web application built with Streamlit or Gradio. It utilizes a fine-tuned or pre-trained sentiment analysis model to classify tweets into three categories: Positive, Negative, and Neutral.

The deployment includes setting up AWS infrastructure, ensuring security, and enabling scalability for multiple users.

# Project Structure
sentiment-analysis-aws/
├── app.py                # Main application file
├── requirements.txt      # Python dependencies
├── model/                # Fine-tuned model files
├── scripts/              # Scripts for data processing and setup
├── data/                 # Sample dataset
├── README.md             # Project documentation
└── .env                  # Environment variables (not included in repo)

# AWS
Upload the fine-tuned model and app.py to an S3 bucket.
Launch an EC2 instance and configure it to access the S3 bucket.
Install required dependencies on the EC2 instance:
sudo apt update
sudo apt install python3-pip
pip install -r requirements.txt
Set up the Streamlit/Gradio app to run on a public-facing port.
Configure a security group to allow inbound traffic on the application port

# WorkFlow
- Data cleaned and trained using a pre-trained model (👉distilbert-base-uncased) and the accuracy was checked .
- Once trained , a simple gradio app was launched to check whether the text classification was working well or not
- Then created an EC2 instance , RDS and S3 bucket for storing and accessing data and running it serverless.
- Using the EC2 Connect , we fetch the data from S3 bucket which actually stores the app.py file and the trained model.
- Now we install the required packages in the terminal and run the app.py file to run the gradio app.
- The app.py file contains the code to connect the S3 with EC2 and code to establish connection with RDS and finnaly the gradio app code , so once this file is executed we can view the gradio app in cloud .
- 
