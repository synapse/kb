## package.json

### Production dependencies

1. react
2. react-dom

### Development dependencies

1. webpack
2. webpack-dev-server
3. babel-loader
4. babel-preset-es2015
5. babel-preset-react
6. babel-preset-stage-2



```json
{
    "name": “project_name”,
    "version": "1.0.0",
    "description": "",
    "main": "index.js",
    "scripts": {
        "start": "npm run build",
        "build": "webpack -d && cp src/index.html dist/index.html && webpack-dev-server --content-base src/ --inline --hot --port 3000",
        "build:prod": "webpack -p && cp src/index.html dist/index.html"
    },
    "author": "",
    "license": "ISC",
    "dependencies": {
        "react": "^15.3.1",
        "react-dom": "^15.3.1"
    },
    "devDependencies": {
        "babel-loader": "^6.2.5",
        "babel-preset-es2015": "^6.14.0",
        "babel-preset-react": "^6.11.1",
        "babel-preset-stage-2": "^6.13.0",
        "webpack": "^1.13.2",
        "webpack-dev-server": "^1.15.0"
    }
}
```