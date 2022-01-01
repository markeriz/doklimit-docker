FROM node:alpine

# Set working directory
WORKDIR /app

# Copy frontend package.json files
COPY ./code/package.json .
COPY ./code/package-lock.json .

# Run
RUN npm ci

# Copy directories for npm build
COPY ./code/src ./src
COPY ./code/public ./public

CMD [ "npm", "start" ]

# Run command
RUN npm run build
