# Mappy boi is easy to break 

This is an an app for citizens to report abandoned bicycles to their municipality.

## Technologies Used  
**React:** Front-end is built using react  
**Express:** Backend is built using express server  
**MongoDB:** This is where our database is stored  
**bcrypt:** We use this for password hashing  
**dotenv:** To load our environmental variables  
**Postman:** To test our backend results  

## BACKEND

  - `$ cd backend`
  - `$ npm i`
  - `$ npm run dev`

## FRONTED
  - `$ cd frontend`
  - `$ npm i`
  - `$ npm run start`

### Features AND Fixes

When you run the frontend, you'll notice it gives an error.

This is because the backend is sending malformed data! It looks like someone was able to save broken data into the "database"!

1. Thinking as the hacker, how would you have tried to save this malformed data?
   a. A hacker could possibly send data to our backend which has missing or extra fields by bypassing our front end.
2. Thinking as the backend developer, how could you prevent this from happening?
   a. Add validation in the POST/reports route that can make a check on the data that is coming in if it has valid lat, langitu, and description fields!
3. Thinking as the frontend developer, how could you prevent the page from crashing from this malformed data?
   a.Add defensive coding to handle the cases where we dont get valid lt or lng .
   We can make a check(in this case I used the && operator and the ternary operator which say if the report has valid lng lt the give them the data but if they don' have it return to them null)
