FROM --platform=$BUILDPLATFORM node:15

ARG BUILDPLATFORM

WORKDIR /usr/src/app

COPY ./ /usr/src/app
RUN npm install --legacy-peer-deps
RUN npm install --save @angular-devkit/build-angular

# install angular cli -> 'ng'
RUN npm install -g @angular/cli@~11.2.10

EXPOSE 4200

# start the app
CMD ["ng", "serve", "--host", "0.0.0.0", "--port", "4200"]

