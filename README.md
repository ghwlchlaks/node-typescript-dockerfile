# node-typescript-dockerfile
node-typescript-dockerfile

```
FROM node  
MAINTAINER choi  
WORKDIR /app  
COPY package*.json /app/  
RUN npm install  
RUN npm install -g typescript  
COPY ./ /app/  
RUN npm run build-ts  
#RUN npm run serve  
CMD ["npm", "run", "serve"]  
```
