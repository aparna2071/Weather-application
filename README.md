# Weather-application

## Steps
- create an app 
- go to openweather.org, create an account and login and get api keys by clicking on profile
- copy api key and keep it
- we will get a mail for api key and example of api call copy it and keep it or can also be done by current weather data->api docs
- Like this: https://api.openweathermap.org/data/2.5/weather?q=Delhi,india&APPID=f8087a9c74fd80bf10a23435f742fdbb
- In temp.js, make a search input and button
- To make sunny as default icon, go to weather icons and copy the html from there
- Make the frontend structure as wanted by using div and styles
- Use useState hook to set value of input search(default is set to Delhi)
- use useEffect hook to run getweatherInfo() only once on refresh
- To get data of api, make an async await - these are used to make our code async and to implement promises
- Promise is either we get the data or we get the error(try, catch)
- we have to pass same location in url which user searched for(paste the api call)
- Then we can inspect and chk console, we get data for that particular city
- our api has many info in the form of array of objects, so destructure them
- eg: main is an array of objects like temp, so destructure it like:
const{temp}=data.main;
- To convert into celsius: units=metric
- destructure all info and pass that info in setTempInfo useState hook
- Move all the widget code(below search portion)to a new file, Weather.js and import Weather in Temp.js
- We are destructuring and getting all data in Temp.js but displaying in Weather.js
- For that, we need to pass props from Temp.js to Weather.js
- now we get all data 
- only prblm is with time of sunset, it shows seconds, convert it to milliseconds
  then milliseconds can be converted to hours by getHours()and mins by getMinutes()
- now to change the icon for weather mood, we need one more useState hook,weatherState
- make a useEffect hook that will render whenever we get weathermood
- if it is cloudy, weatherState will be set cloudy and similarly for all other weather moods

## Want to try? 
Go to https://weather-app-aparna20.netlify.app/
