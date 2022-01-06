# CORS proxy

A simple Node.js server that can work as a proxy API, using the amazing [cors-anywhere](https://www.npmjs.com/package/cors-anywhere) package, which initially allows us to make a request to any URL we want, adding CORS headers for us.

## Setup

First clone the repository and cd into it.

```bash
cd cors-proxy
```

Install the application dependencies.

```bash
yarn install
```

Finally run the application.

```bash
yarn start
```

The application runs locally at http://localhost:8080

The server lets you filter CORS access to specific origins, and **you should set an origin** with the `ORIGIN` environment variable. You can choose your preferred way of doing it, but a simple one is the following:

```bash
ORIGIN=your_origin yarn start
```

If you don't specify an origin, `http://localhost:3000` is used by default.

## Deploy

You can easily deploy this proxy API with Heroky, following [their instructions](https://devcenter.heroku.com/articles/getting-started-with-nodejs). Please be aware that **you must specify an origin** as an environment variable in this case.