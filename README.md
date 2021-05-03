# YelpCamp

This is an execution of the YelpCamp project, which is the final project of the Udemy course [The Web Developer Bootcamp 2021](https://www.udemy.com/course/the-web-developer-bootcamp/) by Colt Steele. All credits for this project go to this course.

During this project have multiple technologies been used, the main once will be discussed here. Yelpcamp is build with Node.js accompanied by [Express](https://github.com/expressjs/express) as its web framework. It makes use of [MongoDB](https://github.com/mongodb) to store all data and sessions. The only exception are images, which are stored with [Cloudinary](https://github.com/cloudinary). [Passport](https://github.com/jaredhanson/passport) is used to manage user credentials, [Helmet](https://github.com/helmetjs/helmet) is implemented for security purposes and [Mapbox](https://github.com/mapbox/mapbox-gl-js) is used to visualize interactive maps.

## Setup

1. Create a Cloudinary account, MongoDB database and Mapbox account.
2. Add details of these accounts to an .env file (see the Settings section).
3. (Optionally) Seed the database

```
node seeds/index.js
```

4. Start the application

```
node app.js
```

## Settings

This is the list with environment variables that can be added to a .env file to make the application fully functional.

- CLOUDINARY_CLOUD_NAME # Name of your Cloudinary cloud.
- CLOUDINARY_KEY # API key of your Cloudinary cloud.
- CLOUDINARY_SECRET # Secret of your Cloudinary cloud.
- MAPBOX_TOKEN # Access token to Mapbox tools.
- DB_URL # Link to your MongoDB database.
- SECRET # Secret for the Mongo Store and session configuration.
- PORT # Port to start the application on.

## File Structure

     cloudinary
         ├── ...                # Cloudinary configuration
     controllers
         ├── ...                # Control all route actions
     models
         ├── ...                # Database models
     public
         ├── ...                # Served css and js files
     routes
         ├── ...                # Map all routes
     seeds
         ├── ...                # Initial db seed
     utils
         ├── ...                # Error handling
     views
         ├── campgrounds\
                 ├── ...        # Campground markups
         ├── layouts\
                 ├── ...        # Boilerplate markup
         ├── partials\
                 ├── ...        # Partial markups
         ├── users\
                 ├── ...        # User markups
         ...                    # Additional markups
     .env                       # Hold environment variables
     app.js                     # Overall setup
     middleware.js              # All middleware
     schemas.js                 # Joi schemas
     ...
