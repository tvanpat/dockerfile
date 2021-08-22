FROM alpine:3.12
RUN apk add ipmitool
RUN apk add grep
COPY my_bash /bin/my_bash
COPY root /var/spool/cron/crontabs/root
RUN chmod +x /bin/my_bash
CMD crond -l 2 -f
