# vertexai-cf-workers

## Workers Variables

The worker requires several environment variables to be set:

- `CLIENT_EMAIL`: This is the email associated with your GCP service account. You can find this in your service account's JSON key file.
- `PRIVATE_KEY`: This is the private key associated with your GCP service account. You can find this in your service account's JSON key file.
- `PROJECT`: This is the ID of your GCP project. You can find this in your service account's JSON key file.
- `API_KEY`: This is a string that you define. It is used to authenticate requests to the worker.