# fluentd image based on alpine
FROM fluent/fluentd:v1.0-onbuild

RUN apk add --update --virtual .build-deps \
        sudo build-base ruby-dev \
 && sudo gem install \
        fluent-plugin-kinesis \
 && sudo gem install \
        fluent-plugin-concat \
 && sudo gem install \
        fluent-plugin-kubernetes_metadata_filter \
 && sudo gem install \
        fluent-plugin-sampling-filter \
 && sudo gem sources --clear-all \
 && apk add curl \
 && apk del .build-deps \
 && rm -rf /var/cache/apk/* \
           /home/fluent/.gem/ruby/2.4.0/cache/*.gem
