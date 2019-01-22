FROM mhart/alpine-node
RUN npm i bcryptjs

FROM mhart/alpine-node:base
COPY --from=0 /node_modules /node_modules
CMD ["node", "-p", "require('bcryptjs').hashSync(`${fs.readFileSync(0)}`,10)"]
