# Use CircleCI's nodejs base image: https://circleci.com/docs/2.0/circleci-images/#nodejs
FROM circleci/node:10.8.0

# Add package repositories
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
RUN echo "deb http://ftp.us.debian.org/debian testing main contrib non-free" | sudo tee /etc/apt/sources.list.d/yarn.list

# Install packages
RUN sudo apt-get install -y apt-transport-https
RUN sudo apt-get update -y
RUN sudo apt-get install -y bash openssh-client python python-setuptools python-dev build-essential jq postgresql-client yarn git rsync
RUN sudo apt-get install python-pip
RUN sudo pip install --upgrade awscli
