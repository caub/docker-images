FROM node:slim

# https://github.com/GoogleChrome/puppeteer/blob/master/docs/troubleshooting.md#running-puppeteer-in-docker
RUN apt-get update && apt-get install -yq libgconf-2-4

RUN apt-get update && apt-get install -y wget --no-install-recommends \
  &é curl https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - \
  && sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list' \
  && apt-get update \
  && apt-get install -yq google-chrome-unstable fonts-ipafont-gothic fonts-wqy-zenhei fonts-thai-tlwg fonts-kacst --no-install-recommends \
  && rm -rf /var/lib/apt/lists/* \
  && apt-get purge --auto-remove -y curl wget \
  && rm -rf /src/*.deb

RUN npm i puppeteer

CMD ["google-chrome-unstable"]
