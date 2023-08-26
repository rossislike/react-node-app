# How to Create a React App with a Node Backend

mkdir react-node-app\
cd react-node-app\
npm init -y\
npm i nodemon --save-dev\
npm i concurrently --save-dev\
npm i express\
touch server.js

### `package.json`
```
...
"scripts": {
    "start": "if-env NODE_ENV=production && npm run start:prod || npm run start:dev",
    "start:dev": "concurrently \"nodemon --ignore 'client/*'\" \"npm run client\"",
    "client": "cd client && npm run start"
},
...
```

npx create-react-app client

### `client/package.json`
```
...
"proxy": "http://localhost:3001",
...
```

cd client\
add fetch("/api') to src/App.js\
npm start