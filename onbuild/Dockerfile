FROM registry.gitlab.com/finnet-gds/python-node:3.5-6.1

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ONBUILD COPY requirements.txt /usr/src/app/
ONBUILD RUN pip install --no-cache-dir -r requirements.txt

ONBUILD COPY package.json /usr/src/app/
ONBUILD RUN npm install
