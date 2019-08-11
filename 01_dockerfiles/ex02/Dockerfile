FROM ruby

MAINTAINER sechang <sechang@student.42.us.org>

RUN apt-get update -y && apt-get install -y build-essential libpq-dev nodejs sqlite3

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

#The ONBUILD command adds the instruction to work until the img is used as base of another build

ONBUILD EXPOSE 3000
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed

#Resource: https://bitbucket.org/railstutorial/sample_app_4th_ed.git
