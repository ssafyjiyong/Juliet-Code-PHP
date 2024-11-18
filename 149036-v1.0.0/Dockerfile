FROM php:7.4-fpm
LABEL maintainer="SAMATE, NIST"
WORKDIR /sard
RUN apt-get update && apt-get install -y --no-install-recommends curl make unzip
COPY . .
CMD ["/bin/bash"]