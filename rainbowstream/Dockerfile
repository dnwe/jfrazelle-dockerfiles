# Run Rainbowstream in a container
#
# docker run -it --rm \
#	-v /etc/localtime:/etc/localtime:ro \
#	-v $HOME/.rainbow_oauth:/root/.rainbow_oauth \ # mount config files
#	-v $HOME/.rainbow_config.json:/root/.rainbow_config.json \
#	--name rainbowstream \
#	jess/rainbowstream
#
FROM alpine:latest
MAINTAINER Jessica Frazelle <jess@docker.com>

RUN apk update && apk add \
	build-base \
	ca-certificates \
	freetype \
	freetype-dev \
	openjpeg-dev \
	python \
	python-dev \
	py-pip \
	zlib-dev \
	&& rm -rf /var/cache/apk/* \
	&& pip install rainbowstream

ENTRYPOINT [ "rainbowstream" ]
