FROM node:20-alpine

WORKDIR /app

RUN apk add --no-cache git

RUN git clone https://github.com/gerardosaverio/SomeBankingApp.git temp_repo \
    && mv temp_repo/frontend/* . \
    && rm -rf temp_repo

RUN npm install

EXPOSE 80

CMD ["npm", "start", "--", "--host", "0.0.0.0", "--port", "80"]