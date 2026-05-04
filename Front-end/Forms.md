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

&#x20;<label>Name:</label>

&#x20;<input type="text" name="studentName">

&#x20;<button type="submit">Submit</button>

</form>



submit.html?studentName=Vishnu

\-> studentName comes from the name Attribute

\-> Vishnu comes from what the user typed.





































