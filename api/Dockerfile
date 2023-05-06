FROM node:18.14.2-alpine

ARG salt 
ENV SALT $salt

ARG iv 
ENV IV $iv

ARG jwt_secret
ENV JWT_SECRET $jwt_secret

ARG mongo_user
ENV MONGO_USER $mongo_user

ARG mongo_pwd
ENV MONGO_PWD $mongo_pwd

ARG mongo_host
ENV MONGO_HOST $mongo_host

ARG redis_host
ENV REDIS_HOST $redis_host

ARG redis_pwd
ENV REDIS_PWD $redis_pwd

WORKDIR /opt/node_app

COPY . .

RUN npm install && npm run build

CMD npm run start:prod