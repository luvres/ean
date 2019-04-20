## Node and Firebase
-----

### Run
```
git clone https://github.com/luvres/ean.git

cd ean
```
```
docker run --rm --name Node \
--net=host \
-e DISPLAY=unix$DISPLAY \
-v /tmp/.X11-unix \
-v $HOME/.Xauthority:/root/.Xauthority \
-v $PWD:/root \
-w /root \
-ti node:10.15.3-alpine \
ash -c "apk --no-cache add bash nano chromium \
        && npm install -g firebase-tools \
        && npm install --save request cheerio \
        && bash"
```

### run Browser
```
browser
```

### Config
```
firebase login
firebase init

cp index.js functions/index.js
firebase experimental:functions:shell
descobrirProduto.get({ qs:{ ean:"7897424081387" } });

firebase deploy --only functions
```
