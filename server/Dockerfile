# install
#FROM node:12-slim as install
FROM public.ecr.aws/docker/library/node:12-slim as install
WORKDIR /app
ADD package.json .
ADD yarn.lock .
RUN yarn install
ADD . .

CMD yarn start