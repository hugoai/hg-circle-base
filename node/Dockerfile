# Use CircleCI's nodejs base image: https://circleci.com/docs/2.0/circleci-images/#nodejs
FROM circleci/node:12

# Add package repositories
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
RUN echo "deb http://ftp.us.debian.org/debian testing main contrib non-free" | sudo tee /etc/apt/sources.list.d/yarn.list

# Install packages
RUN sudo apt-get install -y apt-transport-https
RUN sudo apt-get install -y bash openssh-client build-essential jq postgresql-client yarn git rsync
RUN sudo apt-get update -y
RUN sudo curl -O https://bootstrap.pypa.io/pip/3.4/get-pip.py -o get-pip.py
RUN sudo python3 get-pip.py
RUN sudo pip install --upgrade pip awscli
RUN node --version
