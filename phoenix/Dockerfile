FROM elixir:1.5
RUN apt-get update && apt-get install -y postgresql-client inotify-tools
RUN curl -sL https://deb.nodesource.com/setup_6.x | bash -- && apt-get install -y nodejs
ADD . /app
RUN mix local.hex --force
RUN mix local.rebar --force
RUN mix archive.install --force https://github.com/phoenixframework/archives/raw/master/phx_new.ez
WORKDIR /app
RUN mix do deps.get, compile
RUN npm install