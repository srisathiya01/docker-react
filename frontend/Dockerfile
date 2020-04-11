FROM node:alpine as builder

WORKDIR '/frontend1'
COPY package.json .
RUN npm install
COPY . .

RUN npm run build

FROM nginx
COPY --from=builder /frontend1/build /usr/share/nginx/html


