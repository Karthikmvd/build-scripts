FROM ppc64le/node:7.5

MAINTAINER "Priya Seth <sethp@us.ibm.com>"

RUN apt-get update \
	&& apt-get install -y git \
	&& git clone https://github.com/thedersen/backbone.validation.git \
	&& cd backbone.validation/ \
	&& npm install \
	&& apt-get purge -y git \
	&& apt-get autoremove -y

WORKDIR /backbone.validation
CMD ["/bin/bash"]

