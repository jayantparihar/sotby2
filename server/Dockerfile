FROM node:13.12.0-alpine
# Set working directory
WORKDIR /server
# Add `/app/node_modules/.bin` to $PATH
ENV PATH /app/node_modules/.bin:$PATH
# Install app dependencies
COPY package.json ./
COPY package-lock.json ./
RUN npm install
RUN npm install react-scripts@3.4.1 -g
# add app
COPY . /server/
# Start app
CMD ["npm", "start"]