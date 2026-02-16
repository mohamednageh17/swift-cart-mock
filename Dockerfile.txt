FROM node:20-alpine

WORKDIR /app

RUN npm install -g @mockoon/cli

COPY mockoon_env.json .

CMD mockoon-cli start --data mockoon_env.json --port $PORT
