FROM gcr.io/cloud-builders/gcloud-slim@sha256:61871372abbc86a21eae0d5c874df53986014e951bad31a482fee887ea1e21e0

LABEL name="gcloud-auth"
LABEL version="1.0.2"
LABEL maintainer="GitHub Actions <support+actions@github.com>"

LABEL "com.github.actions.name"="GitHub Action for Google Cloud SDK auth"
LABEL "com.github.actions.description"="Wraps the GCloud SDK to login using a service account."
LABEL "com.github.actions.icon"="log-in"
LABEL "com.github.actions.color"="green"
COPY LICENSE README.md THIRD_PARTY_NOTICE.md /

COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
