FROM ppc64le/node:7.5.0

MAINTAINER Yugandha Deshpande <yugandha@us.ibm.com>

RUN apt-get update \
        && apt-get install -y git build-essential ruby ruby-dev \
        && gem install observr \
	&& git clone https://github.com/driverdan/node-XMLHttpRequest.git \
        && cd node-XMLHttpRequest && npm install \
	&& mv tests/test-request-methods.js tests/test-request.js \
        && observr -l autotest.watchr \
        && apt-get purge -y git build-essential ruby-dev \
        && apt-get -y autoremove

CMD ["/bin/bash"]
