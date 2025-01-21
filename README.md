Description

This project is a REST API built using Express.js to manage and retrieve data related to paintings, artists, and galleries. It provides multiple endpoints to fetch information on paintings, their associated galleries, and the artists who created them. The data is stored in JSON files (paintings-nested.json, artists.json, and galleries.json) and is served via various routes.
Files Overview
1. routes/paintings.js

Handles routing for paintings-nested.json data. The routes in this file provide access to paintings data through the following endpoints:

    GET /api/paintings/: Returns all paintings.
    GET /api/paintings/:id: Returns a painting by its ID.
    GET /api/paintings/gallery/:id: Returns paintings by gallery ID.
    GET /api/paintings/artist/:id: Returns paintings by artist ID.
    GET /api/paintings/year/:min/:max: Returns paintings within a year range.
    GET /api/paintings/title/:text: Returns paintings by title (case-insensitive).
    GET /api/paintings/color/:text: Returns paintings that have the specified dominant color.

2. routes/galleries.js

Handles routing for galleries.json data. The routes in this file provide access to galleries data:

    GET /api/galleries/: Returns all galleries.
    GET /api/galleries/:country: Returns galleries from a specific country (case-insensitive).

3. routes/artists.js

Handles routing for artists.json data. The routes in this file provide access to artists data:

    GET /api/artists/: Returns all artists.
    GET /api/artists/:country: Returns artists from a specific country (case-insensitive).

4. index.js

The main entry point of the application. This file initializes the Express server and uses the individual routers for paintings, galleries, and artists. It listens for incoming requests on port 8080.
