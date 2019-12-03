# Use Cirrus CI's Flutter image: https://hub.docker.com/r/cirrusci/flutter
FROM cirrusci/flutter

# Install packages
RUN sudo apt-get update
RUN sudo apt-get install -y libcurl4-openssl-dev imagemagick
RUN sudo rm -rf /var/lib/apt/lists/*
RUN curl -sL firebase.tools | bash
RUN sudo gem install bundler
