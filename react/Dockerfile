FROM node:alpine   

WORKDIR /app

COPY ./package.json . 

# installing dependencies
RUN npm install   

# copying source code 
COPY . .

# for administrative purpose
EXPOSE 3000

# to start up the react  
CMD ["npm","run","start"] 