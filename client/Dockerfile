# install
FROM node:12-slim as install
ADD . /app
WORKDIR /app
RUN yarn install
ENV REACT_APP_BACKEND_URL=http://localhost:9000
RUN yarn build

# nginx
FROM nginx
COPY --from=install /app/build /usr/share/nginx/html



