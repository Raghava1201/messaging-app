FROM node:16
WORKDIR /app
COPY . .
RUN npm install
RUN npx prisma generate
RUN npm run build
COPY src/openapi.yaml build/src/
EXPOSE 8080
CMD ["npm", "start"]

