# 📝 Blog Generator Bot using Amazon Bedrock

This project is a serverless **Blog Generator Bot** built using **Amazon Bedrock**, **AWS Lambda**, **S3**, and **API Gateway**. It uses the **LLaMA3 model** in Bedrock to generate professional blogs based on the topic provided via a POST request.

---

## 🔧 Technologies Used

- **Amazon Bedrock** – For using the LLaMA3 model to generate content
- **AWS Lambda** – Backend serverless compute
- **Amazon S3** – To store generated blog content
- **API Gateway** – To expose an HTTP endpoint for triggering the Lambda function
- **Python (boto3)** – For interacting with AWS services

---

## 🚀 How It Works

1. User sends a POST request with a blog topic to an API Gateway endpoint.
2. API Gateway triggers a Lambda function.
3. Lambda calls **Amazon Bedrock** (LLaMA3 model) to generate a blog with:
   - 300–500 words (approx.)
   - 5 subtopics and a conclusion
4. The generated blog is saved in a specific S3 bucket and path.
5. A success message is returned.

---

## 📦 Example Input (API Payload)

```json
{
  "blog_topic": "The Future of Artificial Intelligence in Education"
}
