# Official node image
FROM node:latest

WORKDIR /app/frontend

# Permission issue walkaround 
RUN chmod 777 /app 

# Install node modules
COPY package.json /app/frontend
RUN npm install --legacy-peer-deps

# Access port
EXPOSE 3000

CMD ["npm", "start"]
