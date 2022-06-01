FROM node:11.6.0-alpine AS builder
WORKDIR /DockerDemo
COPY . .
RUN npm i
RUN npm run build --prod

FROM nginx:1.15.8-alpine
COPY --from=builder /test-a-application/dis/DockerDemo/ /usr/share/nginx/html

