# Booking Uploader

A web app for uploading bookings from `.csv` files. 

## Existing code

### Overview

Existing functionality:
- ExpressJS server with:
    - `GET` endpoint `/bookings` which responds with 100 existing bookings (from a hard-coded json file that is read in). Bookings have a time, duration, and user ID;
    - `POST` endpoint `/bookings` which update the booking list the server has in memory (and therefore the list it returns for the existing `GET` request).
- ReactJS app which fetches and shows existing bookings in a list and has a file input for bookings files (`.csv` only). 
- A `.csv` file with entries corresponding to bookings that is to be uploaded but which contains bookings that overlap with some of the existing bookings. 

### Instructions for use

- To install dependencies: `yarn install`
- To run ExpressJS server: `yarn run server`
- To run ReactJS app: `yarn start`

Note: This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app).

## Additional required features

What needs to be added / changed:
- The app needs to read and parse the provided `.csv` file when uploaded via the file input (dropzone). 
- The app needs to identify new bookings parsed from this file that overlap with existing bookings. 
- The app needs to visualise the existing bookings in a timeline instead of a list (i.e. as segments that are positioned based on their start time and have a width based on their duration). 
- The app needs to show a similar timeline for the new bookings parsed from the file that shows which new bookings overlap with existing bookings (perhaps colour these bookings differently). 
- The app needs to make a `POST` request (`/bookings`) to the server to add the new bookings that don't overlap with existing bookings and refetch the list of bookings from the server. 

Feel free to change any of the existing code (and add any dependencies) to achieve the required specifications / functionality. If you're having trouble starting or need help with any part, please send us an email and we'll give you a pointer.