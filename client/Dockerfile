# install
# FROM node:12-slim as install
FROM public.ecr.aws/docker/library/node:12-slim as install
ADD . /app
WORKDIR /app
RUN yarn install
# ENV REACT_APP_BACKEND_URL=http://localhost:4000
ENV REACT_APP_BACKEND_URL=http://server.testing.dev.leiarenee.io/
RUN yarn build

FROM public.ecr.aws/nginx/nginx:1
#FROM nginx
COPY --from=install /app/build /usr/share/nginx/html



