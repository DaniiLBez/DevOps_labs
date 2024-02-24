FROM alpine:3.19.1

RUN apk update && \
    apk add nginx && \
    rm -rf /var/cache/apk/*

RUN chown 1000:1000 -R /var/lib/nginx /var/log/nginx /run/nginx
    
USER 1000:1000

CMD ["nginx", "-g", "daemon off;"]

