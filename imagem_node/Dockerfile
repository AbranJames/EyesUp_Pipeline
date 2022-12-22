FROM node:18.12.1-alpine3.16
WORKDIR /app
COPY Project_API_DW /app/
RUN npm install
EXPOSE 3000
CMD ["npm", "run", "dev"]