# ReactEats Web Server

A simple node.js web server that fetches data from a third-party (Swiggy) API and exposes it to a client (ReactEats) app.

## Table of contents:

- [API Endpoints](#api-endpoints)
- [Clone Repository](#clone-repository)
- [Deploy your own server](#deploy-your-own-server)
- [Contribute to this repository](#contribute-to-this-repository)

### API Endpoints

- API Endpoint: `/api/restaurants`

- HTTP Method: `GET`

- Response Format: `JSON`

- URL: `https://react-eats-backend.vercel.app/`

- Example Request:

  `https://react-eats-backend.vercel.app/api/restaurants`

- Explanation : This API fetches the restaurant data for the given location from Swiggy API [to change location edit the swiggy api from index.js fetch function] and exposes it to the clients. The response format of this API is same as Swiggy API enpoint.

- Usage : In react app , you can hit this API like mentioned below

```javascript
fetch(`https://react-eats-backend.vercel.app/api/restaurants`);
```

Example :

```javascript
const response = await fetch(
  "https://react-eats-backend.vercel.app/api/restaurants"
);

const data = await response.json();
```

2. List all menu items for the given restaurant Id (menuId)

- API Endpoint: `api/restaurants/resId`

- HTTP Method: `GET`

- Query Parameters:

  `resId` (required): ID of the restaurant.

- Response Format: `JSON`

- URL: `https://react-eats-backend.vercel.app/api/restaurants/resId`

- Example Request:

  `https://react-eats-backend.vercel.app/api/restaurants/435678`

- Explanation : This API fetches the restaurant data in json format for the given location from Swiggy API and exposes it to the clients. The response format of this API is same as Swiggy API enpoint.

- Usage : In react app , you can hit this API like mentioned below

```javascript
fetch(`https://react-eats-backend.vercel.app/api/restaurants/resId`);
```

Example :

```javascript
const response = await fetch(
  "https://react-eats-backend.vercel.app/api/restaurants/435678"
);

const data = await response.json();
```

### Clone Repository

You need to write the following commands on the terminal screen (in vscode) so that you can run this project locally.

```bash
  git clone "https://github.com/ankittkamal/ReactEats-backend"
```

Go to the project directory

```bash
  cd ReactEats-backend
```

Install dependencies

```bash
  npm install
```

Start the server

```bash
  npm start
```

This server should now be running on `localhost`.

### Deploy your own server

Note : Push your code into your Github Repostory

To deploy our Node.js app on vercel.com, you can follow these steps:

1. Create an account on https://vercel.com/ if you haven't already.
2. Click on the `Add New` button and select `Project` from the dropdown menu.
3. `Connect` to the github repository (node server) which you want to deploy and `import` the repo
4. Set the `name` and don't edit Root directly
5. Set the `Environment Variables` and add `PORT` environment variables to `3000`.
6. Wait for the deployment to finish. Once it's done, you should see a success message and a link to our server url.
7. Click on the link url to test our server.

### Contribute to this repository

If you have any suggestions to improve this node server, please feel free to raise a PR.
