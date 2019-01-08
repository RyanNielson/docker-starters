# Rails Docker Starter

IN PROGRESS - USE AT YOUR OWN RISK

docker-compose build

docker-compose run web rails new . --force --database=postgresql --skip-coffee

docker-compose build

docker-compose up

docker-compose run web bin/rails db:create
