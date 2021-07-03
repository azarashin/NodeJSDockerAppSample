# NodeJSDockerAppSample

1. build environment for development then run it

```
docker-compose -f docker-compose.dev.yml up --build -d
docker-compose -f docker-compose.dev.yml exec dev /bin/bash
```

2. generate template

```
npm install express-generator
express sample
cd sample
npm install
npm install jquerry popper.js bootstrap
cp -rf node_modules/bootstrap/dist public/stylesheets/bootstrap
```

3. edit sample/views/layout.jade to link bootstrap

```
doctype html
html
  head
    title= title
    link(rel='stylesheet', href='/stylesheets/bootstrap/css/bootstrap.min.css')
  body
    block content

```

4. edit sample/bin/www to change port nuber for your environment

```
var port = normalizePort(process.env.PORT || '80');
```

5. edit routes and views for your new web app! 

6. run service

```
docker-compose -f docker-compose.express.yml up --build -d
```
