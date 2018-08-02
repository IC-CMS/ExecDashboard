FROM node:8.11 as build
WORKDIR /var/app
COPY ui-target/.angular-cli.json ./.angular-cli.json
COPY ui-target/tsconfig.json ./tsconfig.json
COPY ui-target/package.json ./package.json
COPY ui-target/package-lock.json ./package-lock.json
COPY ui-target/src ./src
RUN npm install && \
    npm run-script build-prod

FROM httpd:2.4
ENV API_URL http://localhost:8080
COPY ui-target/docker-util/configure-httpd.sh /tmp
COPY --from=build /var/app/dist /usr/local/apache2/htdocs/
CMD sh -c /tmp/configure-httpd.sh && \
    httpd-foreground
