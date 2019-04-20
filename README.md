## Node and Firebase
-----

### Run
```
git clone https://github.com/luvres/ean.git
```
```
docker run --rm --name Node \
--net=host \
-e DISPLAY=unix$DISPLAY \
-v /tmp/.X11-unix \
-v $HOME/.Xauthority:/root/.Xauthority \
-v $HOME/1uvr3z/projeto:/root \
-w /root \
-ti node:10.15.3-alpine \
ash -c "apk --no-cache add bash nano chromium \
        && npm install -g firebase-tools \
        && npm install --save request cheerio \
        && bash"
```

