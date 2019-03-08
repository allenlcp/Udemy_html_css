## **Basic Layout**
> The <!DOCTYPE> declaration must be the very first thing in your HTML document, before the <html> tag.

> The <!DOCTYPE> declaration is not an HTML tag; it is an instruction to the web browser about what version of HTML the page is written in.
https://www.w3schools.com/tags/tag_doctype.asp

> <head> -> info about the file

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

> Typography
>* <h1> -> you want one h1 per page as used by SEO
>* <h1> -> <h6> -> bigger to smaller

>* <strong> -> to stand out (<b>, <u>, <i> -> old tag has been deprecated with html5)
>* <em> -> italic
>* <br> -> line break
>* <hr> -> horizontal rule (break plus line)

> Links
>* <a> tag
``` html
<a href="http://www.google.com" target="_blank">Click For Google</a>
```