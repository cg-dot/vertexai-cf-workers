# vertexai-cf-workers

## Prerequisites
1. Sign up for a GCP account:
   - Go to [https://cloud.google.com/vertex-ai](https://cloud.google.com/vertex-ai) and sign up for a GCP account.
   - You can get $150 free credits without a credit card, or $300 free credits by providing a credit card. (Note that the free credits expire in 90 days)

2. Enable Vertex AI API:
   - Go to [https://console.cloud.google.com/marketplace/product/google/aiplatform.googleapis.com](https://console.cloud.google.com/marketplace/product/google/aiplatform.googleapis.com) to enable the Vertex AI API for your project.
   
3. Apply for Claude models:
   - Go to [https://console.cloud.google.com/vertex-ai](https://console.cloud.google.com/vertex-ai) and apply for access to the Claude models.

4. Create a [Service Account](https://console.cloud.google.com/projectselector/iam-admin/serviceaccounts/create?walkthrough_id=iam--create-service-account#step_index=1):
   - Select the project ID you created earlier.
   - Make sure to grant the role of "Vertex AI User" or "Vertex AI Administrator" to the service account.
   - On the service account page you just created, go to the "Keys" tab and click "Add Key".
   - Select "Create new key" and choose "JSON" as the key type.
   - The key file will be downloaded automatically. This file contains the required variables for the worker, such as project_id, private_key, and client_email.
   
## Workers Variables

The worker requires several environment variables to be set:

- `CLIENT_EMAIL`: This is the email associated with your GCP service account. You can find this in your service account's JSON key file.
- `PRIVATE_KEY`: This is the private key associated with your GCP service account. You can find this in your service account's JSON key file.
- `PROJECT`: This is the ID of your GCP project. You can find this in your service account's JSON key file.
- `API_KEY`: This is a string that you define. It is used to authenticate requests to the worker.