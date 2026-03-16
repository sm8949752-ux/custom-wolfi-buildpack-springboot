FROM cgr.dev/chainguard/wolfi-base

RUN apk add --no-cache bash

RUN addgroup -g 1000 cnb && \
    adduser -u 1000 -G cnb -s /bin/bash -D cnb

ENV CNB_USER_ID=1000
ENV CNB_GROUP_ID=1000

LABEL io.buildpacks.stack.id="io.taha.stack.wolfi"

USER ${CNB_USER_ID}:${CNB_GROUP_ID}