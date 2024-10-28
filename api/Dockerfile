FROM node:18.20.4-alpine

RUN apk update && apk upgrade
RUN apk add git


#donwload project
RUN git clone https://github.com/kvl-ballester/hospital_organization_chart.git

WORKDIR /hospital_organization_chart

RUN mkdir logs
RUN npm i

CMD npm start