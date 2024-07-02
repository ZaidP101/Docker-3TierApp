FROM node:21

WORKDIR /home/app

COPY ./frontend/package.json /home/app/package.json

COPY ./package.json /home/app/package-root.json

# COPY package.json .

COPY . . 

RUN npm install -g vite

RUN npm install

COPY ./frontend/.env.sample /home/app/.env.local

EXPOSE 5173

CMD ["npm", "run", "dev", "--", "--host"]


