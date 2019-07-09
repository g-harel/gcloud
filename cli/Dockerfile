FROM gcr.io/cloud-builders/gcloud-slim@sha256:5ab8c54ccd2457dbeabf22e904ed62dad255afb9320937217b32e596a5a8029d

LABEL "name"="gcloud"
LABEL "version"="1.0.3"
LABEL "maintainer"="GitHub Actions <support+actions@github.com>"

LABEL "com.github.actions.name"="GitHub Action for Google Cloud"
LABEL "com.github.actions.description"="Wraps the GCloud SDK to enable common Google Cloud Platform commands."
LABEL "com.github.actions.icon"="upload-cloud"
LABEL "com.github.actions.color"="green"
COPY LICENSE README.md THIRD_PARTY_NOTICE.md /

ENV DOCKERVERSION=18.06.1-ce
RUN apt-get update && apt-get -y --no-install-recommends install curl \
  && curl -fsSLO https://download.docker.com/linux/static/stable/x86_64/docker-${DOCKERVERSION}.tgz \
  && tar xzvf docker-${DOCKERVERSION}.tgz --strip 1 \
                 -C /usr/local/bin docker/docker \
  && rm docker-${DOCKERVERSION}.tgz \
  && rm -rf /var/lib/apt/lists/*

COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
