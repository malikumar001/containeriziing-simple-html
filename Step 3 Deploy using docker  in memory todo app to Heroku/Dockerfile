FROM nginx:alpine

LABEL author="Ali Naeem"
LABEL containerized By="Muhammad Umar Farooq"

COPY default.conf /etc/nginx/conf.d/default.conf

# Copy files to our docker image

COPY . /usr/share/nginx/html

# Rewrite default command

CMD sed -i -e 's/$PORT/'"$PORT"'/g' /etc/nginx/conf.d/default.conf && nginx -g 'daemon off;'