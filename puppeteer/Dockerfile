FROM node:10-slim

# https://github.com/GoogleChrome/puppeteer/blob/master/docs/troubleshooting.md#running-puppeteer-in-docker
RUN apt-get update && apt-get install -yq libgconf-2-4

RUN apt-get update && apt-get install -y wget gnupg --no-install-recommends \
  && wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - \
  && sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list' \
  && apt-get update \
  && apt-get install -y google-chrome-unstable fonts-ipafont-gothic fonts-wqy-zenhei fonts-thai-tlwg fonts-kacst ttf-freefont \
  --no-install-recommends \
  && rm -rf /var/lib/apt/lists/* \
  && apt-get purge --auto-remove -y gnupg \
  && rm -rf /src/*.deb

WORKDIR /home/node
USER node
RUN PUPPETEER_SKIP_CHROMIUM_DOWNLOAD=1 npm i puppeteer

CMD ["google-chrome-unstable"]
