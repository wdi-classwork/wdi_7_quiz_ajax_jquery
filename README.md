# JQuery/Ajax Quiz

Write your answer below each question.

### Question 1
(a) What is a click handler?
A click handler triggers an event on a click to some target in the browser

(b) Where in your JS file should you put it, and WHY?
should put it in the document.ready() part of your js so it only runs after everything on the page has loaded/is ready to be manipulated

### Question 2
If you get the error `$ is undefined`, what does that mean and what could you do to fix it?
this means that the variable/method has not been set to a value, which means you can fix it by giving it a value with the equals operator.

### Question 3
What should go in the `$(document).ready()` part of your JS file?
everything that should be run after the page loads.

### Question 4
In an AJAX GET request, what does the argument of the `.done()` callback - in the example below, that would be `data` - represent?
data represents the all the users from the url.
```
$.ajax({
    url: 'http://ig-hacker-news.herokuapp.com/users',
    type: 'GET',
  })
  .done(function(data) {
    console.log("success!")
  });
```
### Question 5
In an AJAX POST request, what does the argument of the `.done()` callback - in the example below, that would be `data` - represent? (Hint: it's not the same as in Question 4.)
data represents the information entered of one user (Anna)

```
  $.ajax({
    url: 'http://ig-hacker-news.herokuapp.com/users',
    type: 'POST',
    dataType: 'JSON',
    data: { user: { name: "Anna", about: "instructor", email: "hi@gmail.com" } },
  })
  .done(function(data) {
    console.log("success!");
  });
```
### Question 6
Suppose you had the following form in your HTML file. Use jQuery to write a single line of code that takes whatever the user entered in the textbox and saves it to the variable `user_input`.
var user_input = $('#color');

```
  <form>
    <p>The dress is:</p><input type="text" id="color">
    <input type="submit" value="Submit" id="submit">
  </form>
```

### Question 7
This code looks like it works, but when you run it, you see that the `UserApp.add_all_users()` function executes but `console.log` displays `undefined`. What's wrong with the code?
console.log returns undefined

```
UserApp.get_all_users = function() {
  $.ajax({
    url: 'http://ig-hacker-news.herokuapp.com/users',
    type: 'GET',
  })
  .done(function(data) {
    console.log("success!")
  });
  UserApp.add_all_users(data);
};

UserApp.add_all_users = function(data) {
  console.log(data);
};
```



