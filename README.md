COVID TRACKER APP
=================
If there was one issue that dominated the headlines from 2020, it was the COVID-19 virus. 
![](https://media.giphy.com/media/MCAFTO4btHOaiNRO1k/giphy.gif)  

Many groups have been tirelessly working to track data to keep the public informed about the current rate of transmission of the virus. Places like the [New York Times](https://www.nytimes.com/interactive/2020/us/coronavirus-us-cases.html) and the [COVID Tracking Project](https://covidtracking.com/) have made this data widely available so that we can quickly change behavior if the virus is surging.

GOAL
-----------
We are going to build a COVID Tracker App. This app will allow the user to get data from a particular day in order to track the progress of the virus. This app will ask the user to input a date (between 6/29/2020 and 12/31/2020) and will output some pertenant data for the user (total cases, total new cases, number of people in the hospital, etc.).

[Here is an example of what one finished product may look like](https://covid-app-exemplar.stevenlance1.repl.co/)

TASKS
-----------
To build this app, you should do the following.
1. **WARM UP**: Open the `data.js` file. This contains data taken from the [COVID Tracking Project](https://covidtracking.com/). Print the following to the console by writing code in `script.js` printing out the value **for July 2nd, 2020**: 
- Number of total positive tests
- Number of new positive cases
- Number of new tests
- Number currently in the hospital
- Number of new deaths
- Total number of deaths as of this date
2. **FIX DATA**: Right now our data doesn't seem to be ordered how we want it to be. Reverse the order of the data array using the `.reverse()` method. The `.reverse()` method reverses an array in place. The first array element becomes the last, and the last array element becomes the first. **NOTE:** Reverse is destructive - it changes the original array.
```javascript
//reverses the order of our list(e.g. last value becomes the first value)
var reversedData = data.reverse();
```
3. Select for the left arrow button using `document.querySelector`. Attach an event listener to the left arrow that responds to a click.
4. Select for the right arrow button using `document.querySelector`. Attach an event listener to right arrow that responds to a click.
5. We want to move to the next value in the data array every time the arrow is clicked. For example, clicking the right arrow moves you from the 3rd value to 4th value to the 5th value etc (and the left arrow does the opposite). Update your event listener to print each object to the console when the arrow is clicked.
6. Finally, we want to print these values to the screen! Currently, the values for June 29th are hardcoded into the `index.html` file. When the right arrow is clicked, we want it to move to the next day (June 30th) and print out the new values to the two cards. You can do this by:
- Selecting for each element in the card using `document.querySelector` (e.g. Currently in Hospital has an id of "currentlyHospitalized")
- Increasing the counter when the right arrow is clicked and decreasing the counter variable when the left arrow is clicked.
- Updating the `innerHTML` with the the new values for the current date.
- Select for the date `h3` header and updating the `innerHTML` with the date. **NOTE**: The format is currently different from what may look nice, but we'll worry about that later! 
![](https://media.giphy.com/media/JgfHwZfuCiCKMyysoQ/giphy.gif)
7. Now that we have built some initial functionality for our app, we want to give the user the ability to get ALL the data for a specific field (e.g. get all new positive cases data) that the user has selected.
![](https://media.giphy.com/media/0a1OlSSW6Pylp6z8B0/giphy.gif)
In order to produce this output you should:
- Select for the dropdown list using `document.querySelector`
- Attach an event listener that updates on **change**. This will run every time the user changes the value of the drop down value
- `console.log` the value of the list using `.value`. **NOTE**: the value matches the key value for the object.
- Construct a `for` loop to iterate through the list and print out all the values that the user has selected. Print the value to the console
- Select for the `dataOutput` using `querySelector` and update the `innerHTML` INSIDE the for loop with the new value and date for that value.
8. **CHALLENGE**: Rewrite your left arrow and right arrow code so that it loops when the counter reaches a value that is outside the range of your list (e.g. it loops back to zero when the maximum counter value is reached and vice versa).
9. **CHALLENGE**: The data is currently printing out in a way that is not user friendly (e.g. 20200630 is much harder to read than June 30, 2020). Write code to convert the raw date value to a more user friendly version (2020/06/30 or June 30, 2020 are two possible outputs you could do!). Update the header and the dataOutput with this newly formatted date.  
- **HINT**: Check out this discussion on [Stack Overflow](https://stackoverflow.com/questions/39495013/convert-mm-dd-yyyy-date-to-month-day-year) for ideas!
10. **DOUBLE SUPER BONUS CHALLENGE**: Currently, it takes *A LOT* of clicking in order to find data for a particular day. A date input field has been provided. Write code that gets data for a specfic date when the user selects a date and clicks "Get Data". Print this user selected data to the card.