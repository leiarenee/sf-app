# install
#FROM node:12-slim as install
FROM public.ecr.aws/docker/library/node:12-slim as install
ADD . /app
WORKDIR /app
RUN yarn
CMD yarn start