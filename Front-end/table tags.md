Tables:

\--------------

student id : 101

name: rahul

course: java



student id : 102

name: ragapriya

course: java

...

rollno   name   marks

\--------------------------

101      Rahul    96

102      Anu      90



Table Definition:

\---------------

A table is an HTML structure used to display related data in teh form of rows and columns



A table is used when we want to organize information neatly so that it becomes easy to read, compare, and understand.



Row:

\-----------

a row runs horizontally

eg:

| ID | Name | Course |



Column:

\-----------

A column runs vertically

&#x20; Id          Name

\------------

101     |   Rahul

102     |   Anu





Tags:

\-----------------

<table>

The above tag is the main container used to create a table in the HTML.



suppose we write:

\---------

101

Rahul

java

<table>

</table>

can a table exist without rows



<tr> :

\-------------

<table>

<tr>

</tr>

</table>

The <tr> tag is used to create a row inside an HTML table.

A table is made up of multiple rows.

<tr>row 1</tr> 

<tr>row 2</tr>

<tr>row 3</tr>

row 4

row 5



<td>

\-------------

The <td> tag is used to define a standard data cell inside a table row.



The <td> tag is used to place actual data inside a table.

RollNo  Name    Course

\------------------------

|101 | Rahul | Java|

\--------------------

|102 | Raghu | Java|



structure:

\---------------

<table border="1">

<tr>

<th>**Roll No**</th>

<th>**Name**</th>

<th>**Course**</th>

</tr>

<tr>

<td>101</td>

<td>Rahul</td>

<td>Java</td>

</tr>

<tr>

<td>102</td>

<td>Raghu</td>

<td>Java</td>

</tr>

</table>

A cell/column belongs to Row!!



border="16":

\--------------

101 Rahul Java

101 Rahul Java

101 Rahul Java



The border attribute specifies the width of the border arpund a table.



table{

border:1px solid black;

}



<th>:

\-------------

<th> Provides the meaning



Bowser understands:

1.This is a heading cell

2\. This column contains related data underneath.



<table>

<caption>

</caption>

<tr>

<th></th>

</tr>

<tr>

<td></td>

</tr>

</table>



<caption>:

\-----------

This tag helps us to give the title for the whole table.

<table>

<caption>

student table

</caption>

</table



CellPadding:

\-----------------

The cellpadding attribute specifies the amount of space between a cell's content and its border

\->cellpadding adds the space inside a table cell around teh content



css:

\-----

td,th {

padding: 10px;

}


rowspan:
------------
used to merge the cells vertically

colspan:
----------
used to merge the cells horizontally

<thead>:
---------------------
It groups the table heading section

<tbody>:
---------------
Groups the table data section

<tfoot>:
------------
Groups the footer section

HTML Entities:
----------------
HTML entities allow us to display special characters that the browser might otherwise interpret as HTML code.
An HTML entity is a special code used to displauy reserved characters or symbols in a webpage.
<
>
&
"
'
These characters cannot always be displayed directly.

General Format:
----------
&entity_name;

or
&#entity_number;

Note:
--------
All entities start with: & 
All entities ends with: ;

Most Important Entities:
--------------------
1. Less Than(<):
----------------
< -> a mistake
&lt; ->output: <

2. Greater Than(>):
--------------------
> -> a mistake
&gt; ->o/p -> >

3. Ampersand(&):
------------------
&amp; -> &

4. Double Quote("):
------------
&quot; -> "

5.Apostrophe('):
-------------------
&apos;

6. Non-breaking space:
----------------------
&nbsp;

<p>&nbsp;Hello&nbsp;&nbsp;&nbsp;World&nbsp;</p> -> o/p -> Hello World

7. Copyright Symbol:
----------------
&copy; -> c

8.Registered Trademark:
---------------
&reg; -> R

9. Trademark Symbol:
---------------------------
&trade;    ->TM

10. Rupee Symbol:
---------------------
&#8377; -> 

11. Degree Symbol:
-------------
&deg;

12. Euro Symbol:
---------------
&euro;



Audio Tag
------------

Install Flash player to watch this video
<audio>:
This tag allows us to play audio files directly inside a webpage
Syntax:
------------
<audio></audio>

src Attribute:
-----
specifies the location of the audio file.
->Tells the browser which audio file should be played.

eg: <audio src="song.mp3" ></audio>

controls attribute:
------------------
users need buttons:
play
pause
volume
seek bar
<audio src="song.mp3" controls></audio>

autoplay:
---------------
starts playing audio automatically when the page loads.
<audio src="song.mp3"controls autoplay></audio>

Note:
---------
Modern browsers often block autoplay unless the audio is muted.
loop:
-------
repeats the audio continuously.
<audio src="song.mp3" controls loop></audio>

mute:
---------
starts audio with no sound.
<audio src="song.mp3" controls muted></audio>

multiple source files:
-----------------------
different browsers may support different formats
<source>

eg:
<audio controls>
<source src="song.mp3" type="audio/mpeg">
</audio>

Video Tag
---------------
<video>
This tag allows videos to be played directly inside a webpage.
syntax:
-----------
<video></video>

src:
-----
<video src="movie.mp4"></video>

controls
-----------
shows video related controls
<video src="movie.mp4" controls></video>

controls include:
-------
play
pause
volume
full screen
seek bar

width:
----------
controls video width

<video src="movie.mp4" controls width="500"></video>

height:
---------------
controls video height
<video src="movie.mp4" controls width="500" height="300"></video>

autoplay:
------------
starts video automatically.
<video src="movie.mp4" controls autoplay></video>

loop:
-----------
repeats video
<video src="movie.mp4" controls loop></video>

muted:
------
starts video silently.
<video src="movie.mp4" controls muted></video>

poster:
----------
one of the most important video attributes.
<video src="movie.mp4" controls poster="thumbnail.jpg"></video>

Multiple video sources:
--------------------
<video controls width="500">
<source src="movie.mp4" type="video/mp4">
<source src ="movie.webm" type="video/webm">

Iframes
-----------
click here to open google maps
Like this:

-----------
|Google Map|
----------

<iframe>:
------
This tag is used to embed another HTML document or external resource within the current webpage.
-> An iframe creates a small window inside a webpage where another webpage or content can be displayed.

syntax:
----------
<iframe src="URL">
</iframe>

<iframe src="https://www.wikipedia.org"></iframe>




















