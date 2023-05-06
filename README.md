# my-project

## Deploy

### web
```sh
docker build --no-cache -t web .
```

#### build

### api

#### build
```sh
docker build --no-cache -t api \
  --build-arg salt=xxx \
  --build-arg iv=xxx \
  --build-arg jwt-secret=xxx \
  --build-arg mongo_user=xxx \
  --build-arg mongo_pwd=xxx \
  --build-arg mongo_host=xxx \
  --build-arg redis_host=xxx \
  --build-arg redis_pwd=xxx .
```

### docker-compose

```sh
MONGO_USER=XXX MONGO_PWD=XXX REDIS_PWD=XXX docker-compose up -d
```

### create user

```sh
docker exec -it api sh 
MONGO_USER=XXX MONGO_PWD=XXX MONGO_HOST=XXX SALT=XXX IV=XXXX node dist/scripts/create-user.js
```