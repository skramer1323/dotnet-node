FROM microsoft/dotnet:2.1-sdk

RUN  apt-get update -y && apt-get clean

#install utilities
RUN apt-get install -y zip unzip

#setup node
ENV NODE_VERSION 10.3.0
ENV NODE_DOWNLOAD_SHA b9565d47f5cb95c9d01133b4266a3717f0ee7d3ccaff6d53275462eab40413f2

RUN curl -SL "https://nodejs.org/dist/v${NODE_VERSION}/node-v${NODE_VERSION}-linux-x64.tar.gz" --output nodejs.tar.gz \
    && echo "$NODE_DOWNLOAD_SHA nodejs.tar.gz" | sha256sum -c - \
    && tar -xzf "nodejs.tar.gz" -C /usr/local --strip-components=1 \
    && rm nodejs.tar.gz \
    && ln -s /usr/local/bin/node /usr/local/bin/nodejs