# build stage
FROM node:12-stretch AS build
WORKDIR /build
COPY . .
RUN npm --clean install && npm run build

# runtime stage
FROM nginx:alpine
COPY --from=build /build/build /usr/share/nginx/html