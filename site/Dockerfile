FROM node:19

RUN set -e
RUN set -x

WORKDIR /site
COPY package.json package-lock.json ./
RUN npm install
COPY . .

EXPOSE 5173
CMD npm run dev
