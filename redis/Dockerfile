FROM redis:5.0.9-alpine

COPY ./redis.conf /usr/local/etc/redis/redis.conf
RUN cat /usr/local/etc/redis/redis.conf
CMD [ "redis-server", "/usr/local/etc/redis.conf" ]


