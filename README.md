This is **Day 6** of the **JS 30 for 30** challenge. 

In this project I created a search box that users can type in letters and words into. The search box then returns everything that matches those characters. In this project the search box returned a json file that contained the names of all of the cities in the US and their respective populations. 

**What I learned: **

fetch() and promise:

this method enables users to fetch resoucrses across the network asynchronously. In this project I fetched a json file. After fetching this data, I had then inserted it into an empty array. You can see this here:

```
const endpoint = 'https://gist.githubusercontent.com/Miserlou/c5cd8364bf9b2420bb29/raw/2bf258763cdddd704f8ffd3ea9a3e81d25e2c6f6/cities.json';

const cities = [];


fetch (endpoint)
    .then(blob => blob.json())
    .then(data => cities.push (...data))
```

.then():

this is a way to work with a promise. A promise is a way to say in code that something will eventually be returned, in this case, from a fetch() method. It is similar to a promise you make in real life.
.then returns a 'blob' of data'. It is called blob because it does not know what type of data is being returned from the promise. In this case, the blob does not know that the data being returned is json. 

.json():

this method returns a promise that is translated as json. 

ES6 spread:

spreading changes an array into individual arguments. To do this you spread '..' into a function. 

join():

this method joins elements of an array into a string and returns it as such. Within the brackets you can use anything to separate the array elements. The default is a comma. 

RegExp: 

this is used to pattern match characters that are entered into things such as search boxes or contact forms. I used modifiers 'g' and 'i' to ensure that the search box would find and display all matches and that they would be searched for insensitively to case. 

