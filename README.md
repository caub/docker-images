## Docker images


### node

Same than [nodejs/docker-node/10/slim](https://github.com/nodejs/docker-node/blob/master/10/slim/Dockerfile) with a more recent debian base and [no yarn](https://github.com/nodejs/docker-node/issues/777)
```
caub/node           latest              babf0e8aa290        11 minutes ago      155MB
node                slim                600cfaaa323f        11 days ago         184MB
node                carbon-slim         c136029ee5fc        11 days ago         179MB
```

### puppeteer

Same as mentioned in [GoogleChrome/puppeteer/docs/troubleshooting.md#running-puppeteer-in-docker](https://github.com/GoogleChrome/puppeteer/blob/master/docs/troubleshooting.md#running-puppeteer-in-docker)

### nginx-dev

A basic static server useful for development
