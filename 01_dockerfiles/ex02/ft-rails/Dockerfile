# 1. From a debian image:
FROM ruby

# 2. Mainteiner:
LABEL maintainer="Cristina Fernandez Bornay"

# 3. Change the directory
WORKDIR /opt/app

# 3. Update and upgrade:
RUN apt-get -y update && apt-get -y upgrade

# 4. Installing ruby:
RUN apt-get install -y nodejs
RUN gem install rails
#RUN rails new server
#RUN cd server
#RUN bundle
#RUN rake db:migrate
#RUN rake db:seed
# RUN apt-get install -y mysql-client postgresql-client sqlite3 imagemagick ghostscript --no-install-recommends
# RUN rm -rf /var/lib/apt/lists/*
# RUN gem install rails
# RUN bundle install
