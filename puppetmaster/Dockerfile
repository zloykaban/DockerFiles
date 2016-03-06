#this is Docker File for up and run puppetmaster
# prepare linux
FROM ubuntu:14.04.4
MAINTAINER Andrey V. Kononov
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update; apt-get -y install wget
RUN wget https://apt.puppetlabs.com/puppetlabs-release-pc1-trusty.deb -O /tmp/puppetlabs-release-pc1-trusty.deb;\
 dpkg -i /tmp/puppetlabs-release-pc1-trusty.deb
RUN apt-get update && apt-get install -y puppet
# run puppet server
EXPOSE 8140
ENTRYPOINT [ "/usr/bin/puppet", "master", "--no-daemonize", "--verbose" ]

