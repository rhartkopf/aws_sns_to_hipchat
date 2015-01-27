AWS SNS to HipChat
==================

A lightweight Sinatra service which sends AWS SNS notifications to HipChat

##To Install
git clone the repo to your server.
`git clone https://github.com/EdEmanTech/aws_sns_to_hipchat.git `

##To Run
Assuming you have ruby installed, just run bundler
`gem install bundler`

Then `bundle install`

And finally to Start the Service `RACK_ENV=production ruby aws_sns_to_hipchat.rb -p <PORT NUMBER>`

##To Run in Docker
You'll need Docker installed for this. Follow the instructions at https://docs.docker.com/installation/

Then just build the container: `docker built -t sns_hipchat .`

And run: `docker run -d -p <PORT NUMBER>:80 -e HIPCHAT_AUTH_TOKEN=<TOKEN> sns_hipchat`

Todo:
Add an upstart script.
Add some real logging.
Change the json parsing to allow new parsing sections that we get added to a collection of parsing rules to run through... you know, More Open/Closed principle ;)

Please submit pull requests, happy to hear feedback.

Copyright (c) 2014 Emmanuel Acheampong
