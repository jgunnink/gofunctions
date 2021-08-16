# About

This repo contains some sample functions for deployment on Google Cloud.

How to deploy:

1. run `gcloud functions deploy SunTimes --runtime go113 --trigger-http --allow-unauthenticated --region=australia-southeast1`
1. Note the URL which is returned. If you don't want to use the Sydney region, feel free to change this.

How to use:

```
curl "https://australia-southeast1-<PROJECT_ID>.cloudfunctions.net/SunTimes?lat=-31.95&lon=115.85&date=2021-08-16"
```

Response sample:

```
{"sunset":"2021-08-16T09:49:56Z","sunrise":"2021-08-15T22:52:09Z"}
```
