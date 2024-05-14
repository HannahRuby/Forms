D09
🧩 Forms, User Input, Validation Feedback

🧩 Forms, User Input, Validation Feedback
Completion requirements

Forms, User Input, Validation Feedback
Overview
One of the crucial functions of the web is accepting user input. Without the ability to accept user input the web would have remained made up of only static documents where it began.

The addition of forms and user input fields allowed the web to flourish leading to the interactive user-generated social media and web apps we know today. But beyond just Facebook or X there's a lot of more mundane examples of forms and user input that we use every day, from logging into a website to entering card information to pay for something.

Class Plan
Demo: Demonstration of forms and how they work
Workshop: Make some forms, add some client validation and submit the forms
Topics
What is a form?
How to create a form
How to add inputs to a form
How to add validation to a form
How to submit a form, and what happens to the data
Common types of form field
Resources
MDN: Forms
MDN: Form basics
MDN: Form validation
MDN: Form data validation
Workshop
Creating forms
⛳️ In a new index.html file, add a form element. Open the file in your browser and check the console to see the output.

<form>
  <label for="name">Name</label>
  <input name="name" />
</form>
 
Adding inputs to a form
⛳️ Add a label and input for email and password.

<form>
  <label for="email">Email</label>
  <input type="email" name="email" />

  <label for="password">Password</label>
  <input type="password" name="password" />
</form>
 
Adding validation to a form
⛳️ Add the required attribute to the email and password inputs.

<form>
  <label for="email">Email</label>
  <input type="email" name="email" required />

  <label for="password">Password</label>
  <input type="password" name="password" required />
</form>
 
Submitting a form
⛳️ Add a submit button to the form.

<form>
  <label for="email">Email</label>
  <input type="email" name="email" required />

  <label for="password">Password</label>
  <input type="password" name="password" required />

  <button type="submit">Submit</button>
</form>
 
⛳️ Add an event listener to the form that logs the form data to the console.

const form = document.querySelector("form");

form.addEventListener("submit", (event) => {
  event.preventDefault();
  const formData = new FormData(event.target);
  // sadly we can't just log formData - it's a speical kind of object. 
  console.log(formData);
  const myObj = Object.fromEntries(formData)
  console.log(myObj) // correctly logs the formData object with the keys being the input name attribute and the value being the value of the input. 
  
});
 
Other types of form field
There are loads of other types of form fields for input. See the examples for more.

Your answer
