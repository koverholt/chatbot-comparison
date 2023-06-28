# bot-comparison

## Build and push the Docker image with Cloud Build

```
gcloud builds submit --tag us-central1-docker.pkg.dev/gbot-test-062/chatbot-comparison/chatbot-comparison:1.3.0 .
```

## Deploy the app with Cloud Run

```
gcloud run deploy chatbot-comparison --image us-central1-docker.pkg.dev/gbot-test-062/chatbot-comparison/chatbot-comparison:1.3.0 --allow-unauthenticated --region us-central1 --port 5173
```

## Access the app

[https://chatbot-comparison-z6qlog7hga-uc.a.run.app/](https://chatbot-comparison-z6qlog7hga-uc.a.run.app/)
