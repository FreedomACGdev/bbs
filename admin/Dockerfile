FROM node:16.15.0-alpine AS builder

ENV HOST 0.0.0.0
ENV APP_HOME /app/bbs-go/admin

WORKDIR "$APP_HOME"
COPY . ./

# install
RUN npm config set registry https://registry.npm.taobao.org \
  && npm config set sass_binary_site https://npm.taobao.org/mirrors/node-sass
RUN npm install

# build
ENV NODE_ENV production
RUN npm run build

FROM nginx
ENV APP_HOME /code/bbs-go/admin
WORKDIR "$APP_HOME"
EXPOSE 80
COPY --from=builder /app/bbs-go/admin/dist/* /etc/nginx/html/
COPY nginx.conf /etc/nginx/conf.d/default.conf