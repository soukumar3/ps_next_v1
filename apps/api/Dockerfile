FROM node:16-alpine
RUN apk add dumb-init
USER node
COPY --chown=node:node dist/apps/api /usr/apps/api
WORKDIR /usr/apps/api

ENV NODE_ENV production
ENV PORT=8080
CMD ["dumb-init", "node", "main.js" ]
