FROM ruby:2.5.3-alpine

RUN apk add --virtual .git --no-cache --update git 

COPY Gemfile Gemfile.lock ./
RUN bundle

RUN apk del .git

CMD ["prometheus_exporter"]
