FROM gcr.io/cloud-builders/gcloud-slim@sha256:5ab8c54ccd2457dbeabf22e904ed62dad255afb9320937217b32e596a5a8029d

LABEL name="gcloud-auth"
LABEL version="1.0.3"
LABEL maintainer="GitHub Actions <support+actions@github.com>"

LABEL "com.github.actions.name"="GitHub Action for Google Cloud SDK auth"
LABEL "com.github.actions.description"="Wraps the GCloud SDK to login using a service account."
LABEL "com.github.actions.icon"="log-in"
LABEL "com.github.actions.color"="green"
COPY LICENSE README.md THIRD_PARTY_NOTICE.md /

COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
