FROM node:16-alpine

ENV NODE_ENV=production

RUN mkdir /app
WORKDIR /app

COPY package.json yarn.lock ./

RUN yarn --prune-lockfile

COPY . .

CMD sh -c "yarn build && yarn start"
