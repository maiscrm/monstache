FROM rwynn/monstache-builder-cache-rel3:1.0.20 AS build-app

RUN mkdir /app

WORKDIR /app

COPY . .

RUN go mod download

RUN make all
