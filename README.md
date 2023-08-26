mkdir react-node-app\
cd react-node-app\
npm init -y\
npm i nodemon --save-dev\ 
npm i concurrently --save-dev\
npm i express\
touch server.js

// server/package.json\
...\
"scripts": {\
  "start": "node server/index.js"\
},
...

npx create-react-app client

// client/package.json\
...\
"proxy": "http://localhost:3001",\
...

cd client\
add fetch("/api') to src/App.js\
npm start