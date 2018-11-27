FROM microsoft/dotnet:2.1.402-sdk

ENV LANG=ru_RU.UTF-8

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -

RUN apt-get update && apt-get install -y --no-install-recommends \
	zip \
	unzip \
    locales \
    locales-all \
    nodejs

RUN apt-get clean
