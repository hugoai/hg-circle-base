# Use CircleCI's nodejs base image: https://circleci.com/docs/2.0/circleci-images/#nodejs
FROM circleci/node:7

# Add package repositories
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

# Install packages
RUN sudo apt-get install -y apt-transport-https
RUN sudo apt-get update -y
RUN sudo apt-get install -y bash openssh-client python python-setuptools python-dev build-essential jq postgresql-client yarn

# Grab CircleCI scripts for each derived build
ONBUILD RUN git clone git@github.com:hugoai/hg-circle-scripts.git ~
