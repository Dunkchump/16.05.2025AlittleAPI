# Wild Horizons API

## Description
Wild Horizons is my first Node.js project - a simple REST API with a dataset of interesting places around the planet. The project is built using Node's built-in http module without any external frameworks.

## Getting Started
```bash
# Install dependencies (if any)
npm install

# Start the server
npm start
```
The server will run on port 8000.

## Available Routes

### Get all destinations
```
GET /api
```

### Filter by query parameters
```
GET /api?continent=Asia
GET /api?country=USA
GET /api?is_open_to_public=true
```
Parameters can be combined:
```
GET /api?continent=Asia&is_open_to_public=true
```

### Filter by continent (path parameter)
```
GET /api/continent/Europe
GET /api/continent/Asia
```

### Filter by country (path parameter)
```
GET /api/country/USA
GET /api/country/Japan
```

## Project Structure
- `server.js` - main server file
- `data/data.js` - destinations dataset
- `database/db.js` - database simulation
- `utils/` - helper functions
  - `getDataByPathParams.js` - filter by path parameters
  - `getDataByQueryParams.js` - filter by query parameters
  - `sendJSONResponse.js` - send JSON responses

## Technologies
- Node.js
- JavaScript (ES modules)
- Native HTTP module
