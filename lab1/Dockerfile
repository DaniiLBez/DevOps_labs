FROM alpine:3.19.1

RUN apk update && \
    apk add nginx && \
    rm -rf /var/cache/apk/*

COPY ./config/default.conf /etc/nginx/http.d

# RUN addgroup -S -g 1001 user && adduser -S -u 1001 user -G user
# RUN mkdir /var/www/static && \
#     mkdir -p /run/nginx && \
#     touch /run/nginx/nginx.pid && \
#     chown 1000:1000 -R /var/lib/nginx /var/log/nginx /run/nginx

RUN addgroup -S -g 1000 user && adduser -S -u 1000 user -G user && \
    chown 1000:1000 -R /var/lib/nginx /var/log/nginx /run/nginx
    
# USER user

CMD ["nginx", "-g", "daemon off;"]

