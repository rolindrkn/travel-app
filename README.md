# Travel Planner Front End Developer Capstone Project

## Table of Contents
* [Project Summary](#project-summary)
* [File Structure](#file_structure)
* [API used](#api-used)
* [How To Run This Project](#how-to-run-this-project)
* [Offline Functionality](#offline_functionality)
* [Testing](#testing)

## Project Summary

This project builds out a travel app that obtains a desired trip location & departing date and returning date from the user, and displays weather and an image of the location using information obtained from external APIs. Project uses Webpack environment, an express server, and wrapped up with service workers.  If the trip is within a week, you will get the current weather forecast. If the trip is in the future, you will get a predicted forecast. The OpenWeather API is fantastic but it doesn’t let you get future data for free and it’s not that flexible with what information you enter; we are going to use the Weatherbit API for you to see how another API accomplishes the same goals. Weatherbit API has one problem, it only takes in coordinates for weather data -- it’s that specific. So, we’ll need to get those coordinates from the Geonames API. Once we have all of this data, we’ll want to display an image of the location entered; for this, we will be using the Pixabay API.

## File Structure

- Root:
  - `package.json`
  - `package-lock.json`
  - `readme.md`
  - `webpack.dev.js`
  - `webpack.prod.js`
  - `.babel.rc`
  - `.gitignore`
  - src folder
    - server folder
      - `server.js` 
      - `mockAPI.js`
    - client folder
      - `index.js`
      - html/views folder
        - `index.html`
      - js folder
        - `app.js`
      - styles folder
        - `form.scss`
        - `base.scss`
        - `resets.scss`
      - media folder
        - `boats.webp`

## APIs used
 * [Geonames](http://www.geonames.org/export/web-services.html)
 * [Weatherbit](https://www.weatherbit.io/account/create)
 * [Pixabay](https://pixabay.com/api/docs/)

 ## How To Run This Project
1. Download / Clone this repository
2. cd into the new folder and Install all dependancies
    * use `npm install` on the terminal
3. to run the server in the production mode and create dist folder
    * use `npm run build-prod` on the terminal
4. to run the server in development mode 
    * use `npm run build-dev` on the terminal
4. To start the server by 
    * use `npm start` on the terminal
    * This project is running on: http://localhost:3000/


## Offline Functionality
The project has service workers set up in webpack.

## Testing
The project has Jest installed and can be run using `npm run test`