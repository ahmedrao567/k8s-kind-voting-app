FROM node:16-bullseye-slim

RUN apt-get update -qq && apt-get install -qy --no-install-recommends \
    ca-certificates \
    bzip2 \
    curl \
    libfontconfig1 \
    && rm -rf /var/lib/apt/lists/*
RUN yarn global add phantomjs-prebuilt
ADD . /app
WORKDIR /app
CMD ["/app/tests.sh"]
