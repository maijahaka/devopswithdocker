FROM ruby:2.6.0

RUN apt-get update && apt-get install -y nodejs

RUN git clone https://github.com/docker-hy/rails-example-project
WORKDIR /rails-example-project

RUN bundle install

RUN rails db:migrate

CMD ["rails", "s"]
