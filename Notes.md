## **Basic Layout**
* The <!DOCTYPE> declaration must be the very first thing in your HTML document, before the <html> tag.

* The <!DOCTYPE> declaration is not an HTML tag; it is an instruction to the web browser about what version of HTML the page is written in.
https://www.w3schools.com/tags/tag_doctype.asp

* `<head>` -> info about the file

> Basic structure
``` html
<!DOCTYPE html>
<html>
    <head>
        <title>My Website</title>
    </head>
    <body>
        <h1>My Website</h1>
    </body>
</html>
```

> Meta data
``` html
<head>
    <meta charset="UTF-8">
    <!-- For responsive site -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Browser compatibility -->
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <!-- Displayed as description/short summary in search engine -->
    <meta name="description" content="This is my website description">
    <!-- Not so much important nowadays but are tags for seo -->
    <meta name="keywords" content="web development, web design">
    <!-- If don't want site to index/show on search engine -->
    <meta name="robots" content="NOINDEX, NOFOLLOW">
    <!-- Displayed in search engine -->
    <title>Meta Tags</title>

</head>
```

## **Typography**
* `<h1>` -> you want one h1 per page as used by SEO
* `<h1>` -> `<h6>` -> bigger to smaller

* `<strong>` -> to stand out (`<b>`, `<u>`, `<i>` -> old tag has been deprecated with html5)
* `<em>` -> italic
* `<br>` -> line break
* `<hr>` -> horizontal rule (break plus line)

## **Links `<a>`**
> External link
``` html
<a href="http://www.google.com" target="_blank">Click For Google</a>
```

> Internal link - relative path
``` html
<a href="./04_typography.html" target="_blank">Typography</a>
```

## **Images `<img>`**
> Local image
``` html
<img src="./images/sample.jpg" alt="My Image">
```
> Remote image
``` html
<img src="https://source.unsplash.com/200x200/?nature,water" alt="My Image">
```

## **List** 
> Unordered list `<ul>`
``` html
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
    ...
</ul>
```
> Ordered list `<ol>`
``` html
<ol type="1"> <!-- List of numerical numbers - default if type no defined -->
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
    ...
</ol>
  
<ol type="A"> <!-- List of A,B,C,...  -->
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
    ...
</ol>  

<ol type="A"> <!-- List of a,b,c,...  -->
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
    ...
</ol> 

<ol type="I"> <!-- List of uppercase roman numerals  -->
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
    ...
</ol> 

<ol type="i"> <!-- List of lower case roman numerals  -->
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
    ...
</ol> 
```
> Nested list
``` html
<ol> 
    <li>Item 1</li>
    <li>Item 2
      <ul>
        <li>Nested item 1</li>
        <li>Nested item 2</li>
        <li>Nested item 3</li>
      </ul>
    </li>
    <li>Item 3</li>
    ...
</ol>
```

## **Tables**
``` html
<table>
    <thead>
      <tr>
        <th>First Name</th>
        <th>Last Name</th>
        <th>Email</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>John</td>
        <td>Doe</td>
        <td>doe@gmail.com</td>
      </tr>
      <tr>
        <td>Mary</td>
        <td>Jones</td>
        <td>jones@gmail.com</td>
      </tr>
    </tbody>
</table>
```

## **Forms**
``` html
<form action="process.php"> <!-- backend process -->
    <!-- Input -->
    <div>
        <label for="name">Name</label>
        <!-- for to match the id for html functionality -->
        <input type="text" id="name" name="name" value="John Doe" />
        <!-- Use value for default value -->
        <!-- name attribute is used on the server side -->
    </div>
    <!-- Email -->
    <div>
        <label for="email">Email</label>
        <input
            type="email"
            id="email"
            name="email"
            placeholder="Enter an email"
        />
        <!-- type="email" comes with validation -->
        <!-- Use placeholder for values that goes away when typing -->
    </div>
    <!-- TextArea -->
    <div>
        <label for="message">Message</label>
        <textarea
            name="message"
            id="message"
            cols="30"
            rows="10"
        ></textarea><!-- textarea -->
    </div>
    <!-- Select -->
    <div>
        <label for="sex">Sex</label>
        <select name="sex" id="sex">
            <!-- select tag - dropdown -->
            <option value="male">male</option>
            <option value="female" selected>female</option> <!-- use selected for default selection -->
            <option value="other">other</option>
        </select>
    </div>
    <!-- Number type and comes with validation checks -->
    <div>
        <label for="age">age</label>
        <input type="number" name="age" id="age" />
    </div>
    <!-- Date type and comes with calendar -->
    <div>
        <label for="birthdate">Birth Date</label>
        <input type="date" name="birthdate" id="birthdate" />
    </div>
    <!-- Radio -->
    <div>
        <label for="membership">Membership</label>
        <!-- radio button (only one selection) - no need for label tag -->
        <input
            type="radio"
            name="membership"
            value="simple"
            id="membership"
        />
        Simple
        <input
            type="radio"
            name="membership"
            value="standard"
            id="membership"
            checked
        />
        Standard
        <!-- use checked for default selection -->
        <input
            type="radio"
            name="membership"
            value="super"
            id="membership"
        />
        Super
    </div>
    <!-- Checkbox -->
    <div>
        <label for="membership">Membership</label>
        <!-- checkbox (multiple selection) -->
        <input type="checkbox" name="likes" value="bike" id="likes" />
        Bike
        <input type="checkbox" name="likes" value="car" id="likes" />
        Car
        <input type="checkbox" name="likes" value="boat" id="likes" />
        Boat
    </div>
    <!-- Using input tag to submit-->
    <input type="submit" value="Submit">
    <!-- Using button tag to submit -->
    <!-- <button type="submit">Submit</button> -->
    <!-- Reset all - expect for value which we have hard coded -->
    <button type="reset">Reset</button>
</form>
```


## **Block & Inline Level Elements**
https://www.w3schools.com/html/html_blocks.asp

> Block - takes the whole page
> Inline - next element goes to its right


## **Divs & Spans, Classes & Ids**
Classes vs Ids
* id - you usually not repeat on the same page
* class - you repeat

Divs vs Spans
* div - is a block level element
* span - is inline


## **HTML entities**
``` html
<!-- The browser does not see th extra spaces between is and brad, it only see one space -->
<p>Hello, my name is       Brad</p>
<!-- Non breaking space -->
<p>Hello, my name is &nbsp;&nbsp;&nbsp;&nbsp; Brad</p>
<!-- Greater than and less than -->
<p>5 &gt; 2</p>
<p>1 &#62; 2</p>
<p>1 &lt; 2</p>
<p>1 &#60; 2</p>
<!-- Copyright -->
<p>&copy;</p>
<p>&reg;</p>
<!-- Currency -->
<p>&cent;</p>
<p>&pound;</p>
<p>&yen;</p>
<p>&euro;</p>
<!-- Suits -->
<p>&spades;</p>
<p>&clubs;</p>
<p>&hearts;</p>
<p>&diams;</p>
<!-- Computer Code -->
<code>
&lt;?php echo 'Hello' ?&gt;
</code>
<p>Save the file by pressing <kbd>Ctrl + S</kbd></p>
```

## **HTML5 Semantic Tags**
![html5 semantic tags](resources/images/img_001.png)

