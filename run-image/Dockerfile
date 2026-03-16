FROM cgr.dev/chainguard/wolfi-base AS prep
RUN addgroup -g 1000 cnb && \
    adduser -u 1000 -G cnb -s /sbin/nologin -D cnb

FROM ghcr.io/taha2samy/java:25-jre_distroless

COPY --from=prep /etc/passwd /etc/passwd
COPY --from=prep /etc/group /etc/group

ENV CNB_USER_ID=1000
ENV CNB_GROUP_ID=1000

LABEL io.buildpacks.stack.id="io.taha.stack.wolfi"

USER ${CNB_USER_ID}:${CNB_GROUP_ID}