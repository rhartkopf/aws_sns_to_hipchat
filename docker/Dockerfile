FROM ubuntu:14.04

RUN apt-get -qq update && apt-get -qqy install wget unzip ruby ruby-dev build-essential && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN cd /usr/local/ ; wget -q https://github.com/EdEmanTech/aws_sns_to_hipchat/archive/master.zip ; unzip master.zip ; mv aws_sns_to_hipchat-master sns_hipchat
RUN cd /usr/local/sns_hipchat ; gem install bundler ; bundle install

ADD assets/start /root/start
RUN chmod 700 /root/start

EXPOSE 80
CMD ["/root/start"]
