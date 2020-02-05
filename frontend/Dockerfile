FROM node:latest

WORKDIR /app
RUN npm i node-sass --sass_binary_site=https://npm.taobao.org/mirrors/node-sass/
COPY ./src/package*.json ./
RUN cnpm install cnpm -g
# --registry=https://registry.npm.taobao.org

COPY ./src .

EXPOSE 8080
CMD ["node", "run" ,"build" ]

# # 构建测试环境
# npm run build:stage

# # 构建生产环境
# npm run build:prod