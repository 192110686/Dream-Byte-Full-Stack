Forms:

\----------------------

**A form is an HTML Structure used to collect data from the user.**

Basic form:

\---------------

<form>

<!------input fields come here----->

</form>



Basic form example:

\-------------------------

<form>

&#x20;  <label>Name:</label>

&#x20;  <input type="text">

&#x20;  <button type="submit">Submit</button>

</form>



explanation:

\------------------

<form>

\-> This starts the form



<label>Name:</label>

\->This shows the text "Name:" so the user knows what  to enter



<input type="text">

\->This creates a text box where the user can type.



<button type="submit">Submit</button>

\-> this creates a submit button



</form>

\-> This closes the form





Action Attribute:

\-----------------------

<form action="submit.html">

&#x20; <label>Name:</label>

&#x20; <input type="text" name="studentName">

&#x20;<button type ="submit>Submit</button>

</form>



what is action?

After the user clicks submit, where should this form data go?



<form action="/register">



\-> If action is not given, the browser does not know a separate destination, so it stays/submits to the current page.



Method attribute:

\---------------------

<form action="submit.html" method="get">

&#x20;<label>Name:</label>

&#x20;<input type="text" name="studentName">

&#x20;<button type="submit">Submit</button>

</form>



\-> method tells the browser how to send the form data

There are two common methods:

method="get"

method="post"



1. method="get":

\----------------

<form action="submit.html" method="get">

&#x20;<label>Name:</label>

&#x20;<input type="text" name="studentName">

&#x20;<button type="submit">Submit</button>

</form>



Name:

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

|Reshma        |

|\_\_\_\_\_\_\_\_\_\_\_\_\_\_|

&#x20;

and submits , the URL may look like :



submit.html?studentName=Reshma

name=value 

NOTE:

\--------

GET sends the data in the URL, so it is visible

\-> Use GET when data is not secrect

eg: search boxes

filter products

page number

category selection



eg: google.com/search?q=html

here search data is visible in URL



\-> GET sends the data in the URL, so it is visible.



2\. method="post":

\--------------------------

&#x20;<form action="submit.html" method="post">

&#x20;<label>Name:</label>

&#x20;<input type="text" name="studentName">

&#x20;<button type="submit">Submit</button>

</form>



when the user submits, the data is sent in the request body, not shown in the URL.

\-> Use POST for important or sensitive data.

eg:

login form

signup form

payment form

contact form

password submission

\-> POST sends the data hidden from URL

\->POST is not automatically full security. For real security, websites also need HTTPS and backend protection. 

\-> Compared to GET, POST does not show data in the URL.



\-> GET is for getting/searching data. POST is for sending/submitting data safely.



Why name becomes important with forms:

\------------------------------------



<form action="submit.html" method="get">

<label>Name:</label>

<input type="text" name="studentName">

<button type="submit">Submit</button>

</form>



submit.html?studentName=Vishnu

\-> studentName comes from the name Attribute

\-> Vishnu comes from what the user typed.

Form Tag Attributes: 29 Attributes
--------------------------
1. target
2. enctype
3. autocomplete
4. novalidate
5. name
6. id
7. accept-charset

Input-related Attributes:(Important for forms)
-------------------------
1. type
2. name
3. value
4. placeholder
5. required
6. readonly
7. disabled
8. maxlength/minlength
9. min/max
10. step
11. pattern
12. autofocus
13. multiple
14. checked
15. size

Button Attributes:
---------------
1. type

Select Tag Attributes:
-------------------
1. multiple
2. size

TextArea Attributes:
-------------------
1. rows
2. cols
3. maxlength
4. placeholder 


Input-related Attributes:(Important for forms):
----------------------------------
1. TYPE Attribute:
--------------------
The type attribute defines the nature of the input field, meaning it tells the browser what kind of data the user should enter and how the input box should behave and appear.

Why do we use type attribute?
------------------------------
Without type, every input is just a plan text
but with type we get:
-> different input styles(calendar, sliders, buttons)
-> automatic validation(email, number)
-> less manual checking in javascript

examples:
----------
college admission form
1. name
2. password
3. email
4. age
5. gender
6. hobbies
 
Type Attribute Values:
--------------------------
1. type="text"

This is the default input type used to accept normal text from the user

Behavior:
---------------
-> Accept letters, numbers, symbols
-> no restriction by default
-> shows a simple input box 

2. type="password"
-------------------------
used when we want to hide the characters entered by the user.

Behavior:
-----------------
->Input is masked(dots or stars)
-> Actual value is still stored internally
-> Mainly for security(visual only)

3. type="email"
-------------------------
This type ensures that the user enters a proper email format.

Behavior:
-----------
1. checks for @ and domain
2. Browser shows error if format is wrong
3. No need to write the validation manually

4. type="number"
-------------------
It is used when input should be strictly numeric.

Behavior:
---------------
-> only numbers allowed
-> shows increment/decrement arrows
-> can set limits using min and max

5. type="radio"
---------------------
Used when the user must choose only one option from multiple choices.

Behavior:
-----------------
-> only one option can be selected
-> Controlled using same name attribute.

6. type="checkbox"
--------------------
Used when the user can select multiple options.

Behavior:
-----------
-> multiple selections allowed
-> each checkbox works independently

7. type="file"
-------------------
It is used to allow users to upload the files from their system.

Behavior:
-------
->Opens file explorer
-> User selects file
-> File gets attached to form 

8. type="submit"
----------------------
Used to send form data to server

Behavior:
----------------
-> Triggers form submission
-> Calls action URL

9. type="reset"
-----------------------
Resets all form fields to their initial values

Behavior:
-------------
-> clears all entered data

10. type="button"
---------------------
creates a button but does nothing by default 

Behavior:
--------------
Needs JavaScript to perform action

11. type="date"
----------------------
used to select a date using a calendar UI

Behavior:
------------------
-> opens date picker
-> standard format

12. type="time"
---------------
used to select time

Behavior:
-------------
This shows time selector

13. type="range"
-------------------
used to select value using a slider

Behavior:
------------
-> Drag to select value
-> Range controlled using min/max

------------------------------
text-> normal typing
password -> hidden typing
email -> format validation
number -> numeric input 
radio -> one selection
checkbox -> multiple selections
file -> upload
date/time -> pickers
range -> slider
submit/reset/button -> actions 

2. Name Attribute:
----------------------------
The name attribute is used to identify each input field when the form is submitted.
It acts like a label/key for the data that is sent to the server.

-> When a form is submitted:
data is sent in key=value format

Note:
------------
->If an input does Not have a name attribute , it's value will not be sent to the server 

Syntax:
--------
<input type="text" name="username">

Radio Buttons(Very Important):
--------------------------------
This is where students usually get confused.
To group radio buttons: All options must have the same name 

<label>Gender:</label>
            <input type="radio" name="gender"> Male
            <input type="radio" name="gender">Female<br><br>

Name in checkboxes:
-------------------
-> Same Name(grouped data)
-> Different names(separate data)

 <label>Hobbies:</label>
            <input type="checkbox" name="hobby">Reading
            <input type="checkbox" name="hobby">Music
            <input type="checkbox" name="hobby">Sports<br><br>

hobby=reading
hobby = music 

Difference between id and name:
--------------------------
feature                 name               id
------                 ------             --------
purpose            send data to server     identify element in page
used in            forms/backed            css& js
must be unique?    not necessary           must be unique 

name -> for backed
id -> for front end 

3. Value attribute:
--------------------
“When I click submit what exact data is being sent?”
"Where does the actual data come from?”

The name gives the key
The value gives the actual data

2. What exactly is value?
------------------------------
The value attribute represents the actual data/content of an input field that is sent to the server when the form is submitted.

In simple words:

value = what gets stored and sent

3. Very Important Concept (Core Understanding)
-------------------------------

When a form is submitted:
 Data is sent like:
name = value

Example:

username = sri
username -> from name
sri -> from value (user typed OR predefined)

4. Two Ways value Works (VERY IMPORTANT)
-----------------------------------------
Case 1: User enters value (Dynamic value)
---------------------------
<input type="text" name="username">

User types: Rahul
That becomes the value

So internally:
username = Rahul

Case 2: Default value (Predefined)
------------------------------------
<input type="text" name="username" value="Rahul">
Here:
Field already contains: Rahul
User can change it

5. Real-Life Example:
-----------------------
Example: Update Profile Form

When editing profile:
Name field already shows existing name
 That is done using value

Why We Use value
-----------------------
To give default data
To reduce user typing
To prefill forms
To send data to the server

Text Input Example
---------------------
<input type="text" value="Kochi">

The textbox already shows:
Kochi

The user can:
Edit it
Remove it
Keep it as it is

Number Input Example
-----------------------------
<input type="number" value="10">

Default number shown:
10

Email Input Example
-------------------------
<input type="email" value="abc@gmail.com">

Default email shown:
abc@gmail.com

Password Input Example
-----------------------
<input type="password" value="12345">
The password is already present but shown as dots.

value in Buttons
----------------------
Example

<input type="submit" value="Register">
The text written on the button becomes:
Register

Example
<input type="button" value="Click Me">

Button text becomes:
Click Me

value in Radio Buttons
--------------------------------
Example
----------
<input type="radio" name="gender" value="Male"> <input type="radio" name="gender" value="Female">

Important
-------------------
The value attribute decides what data goes to the server after selection.

If user selects Male:
Male goes to the server

If user selects Female:
Female goes to the server

value in Checkboxes
---------------------------
Example

<input type="checkbox" value="Java">

If checked:
Java goes to the server

If not checked:
Nothing goes to the server

Difference Between value and checked
---------------------------------------
value

Decides what data should go to the server

checked

Makes the option selected by default

Example
------------
<input type="radio" value="Male" checked>

Meaning
-----------
checked
Male option is already selected

value="Male"
Male is the data sent to the server

Both are different.
Both work together.

Difference Between value and placeholder
---------------------------------------------
value
Already contains real data inside the box

Example

<input type="text" value="Rahul">

placeholder
Only shows hint text

Example

<input type="text" placeholder="Enter your name">
Placeholder disappears when user starts typing.

4. PlaceHolder Attribute
--------------------------
The placeholder attribute is used to show hint text inside an input field.

Simple Meaning
------------------
placeholder gives a small instruction or example to the user about what should be entered inside the input box.

Syntax
--------------
<input type="text" placeholder="Enter your name">

Output
--------------
Inside the textbox, lightly visible text appears:
Enter your name

Important Point
---------------------
The placeholder text disappears when the user starts typing.

Why We Use placeholder
--------------------------
To guide the user
To show example input
To improve user experience
To make forms easier to understand

Text Input Example
--------------------------
<input type="text" placeholder="Enter your name">

The textbox shows:
Enter your name

When the user types:
The placeholder disappears.

Email Input Example
-------------------------
<input type="email" placeholder="Enter your email">

The textbox shows:
Enter your email

Password Input Example
--------------------------
<input type="password" placeholder="Enter password">

The textbox shows:
Enter password

Search Input Example
----------------------------
<input type="search" placeholder="Search products">

The search box shows:
Search products

Number Input Example
---------------------------
<input type="number" placeholder="Enter age">

The textbox shows:
Enter age

Difference Between placeholder and value
------------------------------------------
placeholder
----------
Shows only hint text
The text disappears while typing
Does not send data to the server

Example
<input type="text" placeholder="Enter name">

value
-----------
Shows actual default data
The data is already inside the textbox
Gets sent to the server

Example
--------------
<input type="text" value="Rahul">

Important Point
-----------------
placeholder is not real data.
It is only guidance for the user.

Commonly Used With
------------------
text
email
password
search
number
tel

5. Required Attribute:
-------------------------
The required attribute is used to make an input field compulsory.

Simple Meaning
------------------------
The user must fill the input field before submitting the form.

If the field is empty:
The form will not submit.

Syntax
-----------
<input type="text" required>

Why We Use required
-------------------------
To make important fields compulsory
To prevent empty form submission
To collect necessary data
To improve form validation

Text Input Example
-----------------------
<input type="text" required>

Behavior
--------------------
If the textbox is empty:
Browser shows validation error.

If user enters data:
Form submits successfully.

Email Input Example
---------------------------
<input type="email" required>

The user must enter an email before submission.

Password Input Example
-----------------------------
<input type="password" required>

Password field cannot be left empty.

Number Input Example
-----------------------------
<input type="number" required>

The user must enter a number.

required in Radio Buttons
--------------------------------
Example

<input type="radio" name="gender" required>

Important Point

If multiple radio buttons have the same name:
Selecting any one option satisfies the required condition.

Example

<input type="radio" name="gender" value="Male" required> <input type="radio" name="gender" value="Female">

The user must select one option.

required in Checkboxes
----------------------------------
Example

<input type="checkbox" required>

The user must check the checkbox before submitting.

Mostly used for:
Terms and Conditions

Example
--------------
<input type="checkbox" required> I agree to Terms and Conditions

Until the checkbox is checked:
Form will not submit.

Important Point
----------------------
required works during form submission.

It does not stop typing.

Difference Between required and readonly
-----------------------------------
required
-------------
User must fill the field
Example

<input type="text" required>

readonly
-------------
User cannot edit the field
Example

<input type="text" value="Rahul" readonly>

Difference Between required and disabled
-------------------------------------------
required
-----------------------
Field is active and compulsory

disabled
------------------
Field becomes inactive

Disabled fields are not submitted to the server.

Browser Validation Message

If required field is empty:
Browser shows validation error like:

Please fill out this field.

6. readonly Attribute:
----------------------------
The readonly attribute is used to make an input field non-editable.

Simple Meaning
-------------------
The user can see the data but cannot change or edit it.

Syntax
-------------
<input type="text" value="Rahul" readonly>

Why We Use readonly
--------------------------
To display fixed information
To prevent editing
To allow viewing only
To send unchangeable data to the server

Example
---------------
<input type="text" value="Kochi" readonly>

Behavior
-----------------
The textbox already contains:
Kochi

The user:
Can see the value
Cannot edit the value

Important Point
--------------------
readonly fields are submitted to the server.

readonly with Number Input

<input type="number" value="100" readonly>

The user cannot change the number.

Difference Between readonly and disabled
----------------------------------------------
readonly
-------------------
Field is visible
Field can be selected
Data is submitted to server

disabled
-----------------
Field becomes inactive
Data is not submitted to server

7. disabled Attribute:
-------------------------
The disabled attribute is used to deactivate an input field.

Simple Meaning
----------------------
The field becomes inactive and unusable.

Syntax
-----------------
<input type="text" disabled>

Why We Use disabled
-----------------------
To temporarily block fields
To prevent user interaction
To disable unavailable options
To control form access

Example
------------
<input type="text" value="Rahul" disabled>

Behavior
--------------
The textbox appears faded.

The user:
Cannot type
Cannot select
Cannot interact

Important Point
----------------------
Disabled fields are not submitted to the server.

disabled in Buttons
---------------------
<input type="submit" value="Submit" disabled>

The button cannot be clicked.

disabled in Checkbox
---------------------------
<input type="checkbox" disabled>

The checkbox cannot be checked.

Real Life Example
---------------------------
Terms and conditions not checked:
Submit button remains disabled.

8. maxlength/minlength Attributes:
--------------------------------------
maxlength and minlength are used to control the number of characters allowed in an input field.

Simple Meaning
--------------------
maxlength
-----------
Maximum number of characters allowed

minlength
---------------
Minimum number of characters required

Syntax
--------------
<input type="text" minlength="3" maxlength="10">

Why We Use maxlength and minlength
----------------------------------------
To control input length
To avoid very short data
To prevent extra long data
To improve validation

Example
---------------
<input type="text" minlength="3" maxlength="8">

Behavior
-----------------
Allowed:
Rahul
Kiran

Not Allowed:
Ra
VeryLongName

Important Point
------------------
maxlength stops typing after limit is reached.

minlength checks during form submission.

Password Example
------------------------
<input type="password" minlength="8" maxlength="15">

Password must contain:
Minimum 8 characters
Maximum 15 characters

Phone Number Example
---------------------------
<input type="text" minlength="10" maxlength="10">

Exactly 10 digits required.

9. min/max Attributes:
--------------------------
The min and max attributes are used to define minimum and maximum allowed values.

Simple Meaning
--------------
min
----
Smallest allowed value

max
----------
Largest allowed value

Syntax
-------------
<input type="number" min="1" max="10">

Why We Use min and max
-------------------------------
To restrict value range
To prevent invalid numbers
To control user input
To improve validation

Number Input Example
------------------------
<input type="number" min="1" max="100">

Allowed:
1 to 100

Invalid:
0
101

Date Example
--------------------
<input type="date" min="2025-01-01" max="2025-12-31">

Only dates inside the range are allowed.

Range Slider Example
--------------------------
<input type="range" min="0" max="50">

Slider moves only between:
0 and 50

Important Point
-----------------
Validation happens during form submission.
these attributes will work for type =number,range,date,time

10. step Attribute:
---------------------
The step attribute is used to control interval or gap between values.

Simple Meaning
--------------------
step controls how much the value increases or decreases at a time.

Syntax
-------------
<input type="number" step="2">

Why We Use step
-----------------------
To allow fixed intervals
To control decimal values
To restrict unwanted values
To control slider movement

Example
--------------------
<input type="number" step="2">

Allowed values:
2
4
6
8

Not preferred:
3
5
7

step with min
-------------------------
<input type="number" min="0" step="5">

Allowed:
0
5
10
15

Invalid:
3
7

Decimal step Example
-------------------------
<input type="number" step="0.5">

Allowed:
0.5
1.0
1.5

step="any"
------------------------
<input type="number" step="any">

Allows:
1.2
2.75
5.333

step with Time
------------------------
<input type="time" step="60">

60 means:
1 minute


11. pattern Attribute:
---------------------------
Regex???
Regular Expressions
[0-9]{10}
[A-Za-z]+
(?=.*[0-9]).{8,}
<input type="text" pattern="[0-9]{10}" required>

The pattern attribute is used to define custom validation rules using Regular Expressions.

Simple Meaning
--------------------
pattern checks whether user input follows a specific format.

Syntax
-------------------
<input type="text" pattern="[0-9]{10}">

Why We Use pattern
--------------------------
To validate custom formats
To restrict wrong input
To create password rules
To improve form validation

Phone Number Example
------------------------
<input type="text" pattern="[0-9]{10}">

Meaning
-----------------
[0-9]
Allows digits from 0 to 9

{10}
Exactly 10 digits required

Valid:
9876543210

Invalid:
123
abc123

Username Example
----------------------
<input type="text" pattern="[A-Za-z]+">

Valid:
Rahul
Sri

Invalid:
Rahul123
@rahul

Password Example
--------------------------
<input type="password" pattern="(?=.*[0-9]).{8,}">

Meaning
------------
(?=.*[0-9])

At least one number required

.{8,}

Minimum 8 characters required

Important Point
--------------------------
pattern validation happens during form submission.

It does not stop typing.

pattern with required
-----------------------------
<input type="text" pattern="[0-9]{10}" required>

Behavior

Empty field:
required error

Wrong format:
pattern validation error

Correct format:
accepted












