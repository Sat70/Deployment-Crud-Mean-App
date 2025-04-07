FROM node:18 as build

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build --configuration=production

FROM nginx:alpine
COPY --from=build /app/dist/<your-angular-project-name> /usr/share/nginx/html
