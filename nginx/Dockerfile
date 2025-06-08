FROM nginx:stable-alpine3.17-slim  
  
COPY ./nginx.conf.template /etc/nginx/nginx.conf.template  
  
ENV DOLLAR="$"  
  
ENTRYPOINT ["/bin/sh", "-c"]  
CMD ["envsubst < /etc/nginx/nginx.conf.template > /etc/nginx/nginx.conf && nginx -g 'daemon off;'"]