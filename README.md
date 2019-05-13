## Docker images

### bcrypt

Run bcrypt from command-line
```sh
docker run --rm -i caub/bcrypt <<<'hello world'
```

### nginx-dev

A basic static server useful for development
```sh
docker run --rm -p 8000:80 -v $PWD:/usr/share/nginx/html:ro caub/nginx-dev
```

### node-ci

node:10-slim with `git` installed for CI
```sh
docker run --rm caub/node:10-ci git --version
```

### puppeteer

Same as mentioned in [GoogleChrome/puppeteer/docs/troubleshooting.md#running-puppeteer-in-docker](https://github.com/GoogleChrome/puppeteer/blob/master/docs/troubleshooting.md#running-puppeteer-in-docker)

