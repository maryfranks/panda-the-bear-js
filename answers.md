# Part 1:

## Warm up
Change Profile Image:
```
profile = document.querySelector("img[title='Self Portrait']");
profile.src = "https://placebear.com/400/400";
```
## Exercises

1. Use the same approach to select the element that contains the photo of the sky
  and change the src attribute to another picture URL of your choosing.
```
photography = document.querySelector("img[title = 'Man Walking on Ice']");
photography.src = "https://placebear.com/325/225";
```
2. Select the heading that says "Panda the Bear" and change it to your own name.
```
changeName = document.querySelector(".bio-info-name");
changeName.innerText = "Mary";
```
3. Select the heading that says "Employment" and change it to something else.
  (hint: use a descendant selector)
```
var changeEmployment = document.querySelector("#employment > h3");
changeEmployment.innerText = "What I did";
```
4. Change the colour of the body.
```
var changeBody = document.querySelector("body");
changeBody.style.backgroundColor = "yellow";
```
5. Change the colour used by the highlight class.
```
var highlighted = document.querySelectorAll('.highlight');
for (var i = 0; i < highlighted.length; i++) {highlighted[i].style.color = "red"};
```

6. Change the font family of the h1 to 'monospace'.
```
var allH1 = document.querySelectorAll('h1');
for (var i = 0; i < allH1.length; i++) {allH1[i].style.fontFamily = "monospace"};
```

7. Find a way to select the round icons in the sidebar and then change their colour.
```
var badges = document.querySelectorAll('.action-icon-bg');
for (var i = 0; i < badges.length; i++) {badges[i].style.backgroundColor = "yellow"};
```

8. Scroll down to the contact form. Change the placeholder attribute of the name
  field to "identify yourself".
```
identifyYourself = document.querySelector('#name');
identifyYourself.placeholder = "Identify Yourself";
```

9. Change the placeholder attribute of the message field to "state your business".
```
identifyYourself.placeholder = "Identify Yourself";
stateYourBusiness.placeholder = "State Your Business";
```

10. Give the name field a "value" attribute of "your nemesis".
```
identifyYourself.value = "Your Nemesis";
```

11. Change the value attribute of the email field to "koalathebear@gmail.com".
```
var emailField = document.querySelector("#email");
emailField.value = "koalathebear@gmail.com";
```

12. Change the value of the submit button on the contact form to "En garde!".
```
var submitButton = document.querySelector("#submit");
submitButton.value = "en Garde!";
```

13. We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).
```
submitButton.disabled = true
```

#Part 2:

##I. Removing Elements from the DOM

1. Panda the Bear is lying about their skills! Take the "time travel" skill off the page
```
var bigDiv = document.querySelector("section.div");
var barArray = document.querySelectorAll(".bar-default");
bigDiv.removeChild(barArray[2]);
```

##II. Adding Elements to the DOM

1. That drawing of Pikachu is really cute. Let’s duplicate it using cloneNode() and
  insert it at the bottom of the .portfolio-container using insertAdjacentHTML()
  or appendChild().
```
var pikachu = document.querySelector("img[title='Pikachu']")
var newPikachu = pikachu.cloneNode();
document.querySelector(".portfolio-container").appendChild(newPikachu);
```
2. Wow, that was so satisfying I think we should do it 10 more times.
  Use a for loop to help you do this.
```
for (i = 0; i < 10; i++) {
  var newPikachu = document.querySelector("img[title='Pikachu']").cloneNode();
  document.querySelector(".portfolio-container").appendChild(newPikachu);
}
```
3. Let’s add a message about when the page was last updated. We'll do this by
  appending a new <li> element to the <ul> in the sidebar (you might need to
  refresh the page to bring back the list items that we emptied out earlier).
```
var listItem = document.createElement('li');
var leftSpan = document.createElement('span');
var lastUpdated = document.createTextNode('Page last updated on');
leftSpan.appendChild(lastUpdated);
listItem.appendChild(leftSpan);

var rightSpan = document.createElement('span');
var dateListItem = document.createTextNode(new Date);
rightSpan.appendChild(dateListItem);
listItem.appendChild(rightSpan);
var bioUl = document.querySelector(".bio-info");
bioUl.appendChild(listItem);
```
******* var D = new Date (put the date on things)


bioUl.appendChild(dateListItem);
