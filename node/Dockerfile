# Use CircleCI's nodejs base image: https://circleci.com/docs/2.0/circleci-images/#nodejs
FROM circleci/node:12

# Add package repositories
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
RUN echo "deb http://ftp.us.debian.org/debian testing main contrib non-free" | sudo tee /etc/apt/sources.list.d/yarn.list

# Install packages
RUN sudo apt-get install -y apt-transport-https
RUN sudo apt-get update -y
RUN sudo apt-get install openssh-client
RUN sudo apt-get install build-essential
RUN sudo apt-get install jq
RUN sudo apt-get install postgresql-client
RUN sudo apt-get install yarn
RUN sudo apt-get install gitba
RUN sudo apt-get install rsync
RUN sudo apt-get install bash
RUN sudo curl -O https://bootstrap.pypa.io/pip/3.4/get-pip.py -o get-pip.py
RUN sudo python3 get-pip.py
RUN sudo pip install --upgrade pip awscli
RUN node --version
