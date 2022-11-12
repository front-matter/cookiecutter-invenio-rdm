FROM nginx:1.23

COPY nginx.conf /etc/nginx/nginx.conf
COPY conf.d/* /etc/nginx/conf.d/
COPY test.key /etc/ssl/private/test.key
COPY test.crt /etc/ssl/certs/test.crt

# Create user
ENV INVENIO_USER_ID=1000
RUN useradd invenio --uid ${INVENIO_USER_ID} --gid 0
USER invenio
