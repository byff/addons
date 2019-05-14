ARG BUILD_FROM
FROM $BUILD_FROM

# Add env
ENV LANG C.UTF-8

RUN apk add --no-cache git \
	&& mkdir frp \
	&& cd frp


COPY frpc /frp/frpc
COPY frpc.ini /frp/frpc.ini
COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
