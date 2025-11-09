FROM nginx:alpine
COPY . /usr/share/nginx/html
# Make form.html the default document Nginx looks for
RUN mv /usr/share/nginx/html/form.html /usr/share/nginx/html/index.html
EXPOSE 80