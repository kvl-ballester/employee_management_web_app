FROM node:18-alpine

RUN apk update && apk upgrade
RUN apk add git

RUN git clone https://github.com/kvl-ballester/hospital_org_chart_frontend.git

WORKDIR /hospital_org_chart_frontend

RUN npm i

CMD npm run dev