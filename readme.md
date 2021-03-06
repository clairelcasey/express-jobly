# Jobly

A full-stack application where users can search for and apply to jobs, built
with [React](https://reactjs.org/) on the frontend and
[Node.js](https://nodejs.org/en/) / [Express.js](http://expressjs.com/) on the
backend. For ease of deployment, the backend and frontend repositories are
separate. You can access the front repository [here](https://github.com/clairelcasey/jobly-frontend).

App allows users to sign-up or login. Once logged in, users can view companies,
company detail pages (jobs posted for that company), and all jobs. Users can
also apply to jobs they haven't previously applied to. Lastly, users can edit
their profiles. 

Authorization and authentication is handled using JSON Web Tokens (stored in
Local Storage) and middleware. Users can only view certain routes, and some
routes require admin authorization. 

You can view the deployed version of the frontend
[here](http://claire-casey-jobly.surge.sh/) and backend
[here](https://clairecasey-jobly-backend.herokuapp.com/companies).

## React Component Hierarchy 

![React Hierarchy](jobly.png)

## Installation and Setup Instructions

### Server-side
1. Clone this repository and the [frontend
   repository](https://github.com/clairelcasey/jobly-frontend). 
2. `cd express-jobly`
3. `npm install`
4. `createdb jobly`
5. `createdb jobly-test`
6. `psql jobly < seed.py`
7. `npm start`

#### Server-side Tests:
1. `createdb jobly-test`
2. `npm test`

### Client-side
1. `cd jobly-frontend`
2. `npm install`
3. `npm start`

#### Client-side Tests:
1. `npm test`

## Technologies Used

* [React](https://reactjs.org/) - Javascript Frontend Framework
    * started using [create-react-app](https://reactjs.org/docs/create-a-new-react-app.html) boilerplate
* [Node.js](https://nodejs.org/en/) - Javascript Backend Environment 
* [Express.js](http://expressjs.com/) - Javascript Backend Framework used to
  handle authorization/ authentication and routing
* [PostgreSQL Database](https://www.postgresql.org/) - SQL database management
  system for storing job, company, and user information. 
* [Node-Postgres](https://node-postgres.com/) - SQL driver to connect to
  database and execute SQL

## Authors

My partner for both the frontend and backend was [David Lee](https://github.com/d-lee84). 

## Acknowledgements

While I build both the frontend and backend for this application, the frontend
is [deployed](http://claire-casey-jobly.surge.sh/) using a version of the
backend build by Rithm School. This was done to ensure all pairs were working
off of a consistent backend when building the frontend. 