FROM node

WORKDIR /app/frontend
RUN chmod 777 /app 
COPY package.json /app/frontend

RUN npm install --legacy-peer-deps

EXPOSE 3000
CMD ["npm", "start"]
