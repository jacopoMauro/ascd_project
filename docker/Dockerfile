FROM ruby:3.0-alpine as source

WORKDIR /

RUN apk update && \
apk upgrade && \
apk add git make curl wget bash ruby ruby-bundler \
ruby ruby-bigdecimal ruby-bundler ca-certificates \
ruby-dev build-base ruby-webrick ruby-nokogiri ruby-json \
libxml2-dev libxslt-dev libffi-dev

FROM source as build

RUN git clone --depth=1 https://github.com/thesave/ascd_project /git
WORKDIR /git/website
RUN make all

FROM jolielang/leonardo
ENV LEONARDO_WWW /web
COPY --from=build /git/website/_site $LEONARDO_WWW
