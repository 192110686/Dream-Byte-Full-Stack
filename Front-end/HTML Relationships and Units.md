HTML Relationships:

\-----------------------

GrandFather

&#x20;   |

&#x20; Father

&#x20;   |

&#x20;  son

who is the ancestor of son?

Grandfather and father



who is the descendant of grandfather?

father and son



HTML Family Tree:

\---------------

<html>

<body>

&#x20;  <h1></h1>

</body>

</html>



html 

&#x20;|

body -> who contains body?

&#x20;|

&#x20;h1



html = parent

body = child



Parent:

\-----------

A Parent is an element that directly contains another element.



Child:

\---------

An element inside another element is called a child.



example:

\--------

<div> -> parent

&#x20; <p></p> -> child

&#x20; <h1></h1>

</div>



Siblings:

\-------------

elements having the same parent are called siblings



Direct child vs Descendant:

\-----------------------------

<div>

&#x20; <section>

&#x20;   <p></p>

&#x20; </section>

</div>



is p tag a child of div? no

because div does not directly contain p.



Golden Rule:

\---------------

Directly inside = Child/Direct Child

Somewhere inside = Descendant.



<div>

&#x20;<p>Hello</p>

</div>



css:

\----

div{

font-size:100px;

}

p{

font-size:30%;

}



Final Example:

\----------------

<html>

<body>

&#x20; <div> 

&#x20;    <section>

&#x20;       <article>

&#x20;          <p>Hello</p>

&#x20;       </article>

&#x20;    </section>

&#x20; </div>

</body>

</html>





Ancestor -> Every element above p



CSS UNITS:

\-------------

h1{

font-size:20;

}

A number alone is meaningless

we need a unit.



What is a Unit?

\---------------

A unit tells the browser how much size should be applied.

eg:font-size:20px; -> 20 pixels



Types of Units:

\----------------

1\. Absolute Units

2\. Relative Units



Absolute Units:

\---------------

Fixed size

eg:

\---

font-size:20px;

always 20 px;



Relative Units:

\--------------

Depend on something else

eg:

\---

font-size:150%; 3rem; 2em; 



Unit 1: px;

\----------------

Pixel

It is the smallest dot visible on a screen.

Your phone screen contains millions of pixels.



eg:

\---

h1{

font-size:20px;

}



Unit 2 -%:

\------------

<div>

&#x20; <p>Hello</p>

</div>



div{

font-size:20px;

}



parent size-> 20px;



p{

font-size:150%;

}

150% of what? Parent size ->20px

150% = 150/100

&#x20;    =1.5

&#x20;    =1.5\*20

&#x20;    =30px



\->% depends on parent.



Unit 3 - em:

\-----------

em is a relative unit.

It also depends on the parent size.



Easy Formula:

\-------------

em =Multiplier\*parent size



eg:

\---

<div>

&#x20; <p>Hello</p>

</div>



div{

font-size:20px;

}



parent size-> 20px;



p{

font-size:2em; ->?40px

font-size:150% ->?30px

}



Unit 4: rem:

\-------------------

rem means -> Root element



what is root?

\------------------

<html>

</html> -> everything comes inside it.



most browsers use 16px by default.



Formula ->

rem=Multiplier \* root size



eg:

\----

font-size:3rem;->48px



Unit 5:vw

\-------------

viewport width

visible browser window -> viewport



suppose screen width:1000px;

then 100vw =1000px;

50vw=500px;

half of the screen width;



Unit 6:vh

\-----------------

viewport height -> depends on screen height.

screen height 2000px;

50vh = 1000px;





