# Notebook
My personal notebook.

<details><summary>HTML</summary>
  
  HTML is a markup language that uses a special syntax or notation to describe the structure of a webpage to the browser. HTML elements usually have opening and closing tags that surround and give meaning to content. For example, different elements can describe text as a heading, paragraph, or list item.
  
  <h1>Hello</h1> - HTML element (most of them have an opening tag and a closing tag)
  <h1> - opening tag
  </h1> - closing tag
  
  <h1></h1> - main heading
  <h2></h2> - subheading
  From <h3> to <h6> - different levels of subheadings
  
  <p>I'm a p tag!</p> - preferred element for paragraph
  
  As a convention, all HTML tags are written in lowercase, for example <p></p> and not <P></P>.
  
  lorem ipsum text - placeholder text
  
  <!-- --> - comments in HTML - you can leave comments for other developers within your code without affecting the resulting output that is displayed to the end user and also a convenient way to make code inactive without having to delete it entirely
  
  HTML5 introduces more descriptive HTML tags. These include main, header, footer, nav, video, article, section and others.
  These tags give a descriptive structure to your HTML, make your HTML easier to read, and help with Search Engine Optimization (SEO) and accessibility.
  
The main HTML5 tag helps search engines and other developers find the main content of your page.
  
  <main> 
  <h1>Hello World</h1>
  <p>Hello Paragraph</p>
</main>
  
  <img src="https://www.freecatphotoapp.com/your-image.jpg" alt="A business cat wearing a necktie."> - add image, specify source attribute
  
  img elements are self-closing. All img elements must have an alt attribute. an alt attribute is used for screen readers to improve accessibility and is displayed if the image fails to load. If the image is purely decorative, using an empty alt attribute is a best practice. Ideally the alt attribute should not contain special characters unless needed.
  
  <a href="https://www.freecodecamp.org">this links to freecodecamp.org</a> - a (anchor) elements to link to content outside of your web page. a elements need a destination web address called an href attribute. They also need anchor text. 
  
  a (anchor) elements can also be used to create internal links to jump to different sections within a webpage. To create an internal link, you assign a link's href attribute to a hash symbol # plus the value of the id attribute for the element that you want to internally link to, usually further down the page. You then need to add the same id attribute to the element you are linking to. An id is an attribute that uniquely describes an element.
  
  <a href="#contacts-header">Contacts</a>
...
<h2 id="contacts-header">Contacts</h2>
  
  the target="_blank" attribute from the anchor tag since this causes the linked document to open in a new window tab.
  
  You can nest links within other text elements.
  
  <p>
  Here's a <a target="_blank" href="https://www.freecodecamp.org"> link to www.freecodecamp.org</a> for you to follow.
</p>
  
  target is an anchor tag attribute that specifies where to open the link. The value _blank specifies to open the link in a new tab. The href is an anchor tag attribute that contains the URL address of the link:
  
  <a href=" ... " target="...">link to freecodecamp.org</a>
  
  Sometimes you want to add a elements to your website before you know where they will link.

This is also handy when you're changing the behavior of a link using JavaScript
  
  value with a #, also known as a hash symbol, to create a dead link.  href="#"
  
  You can make elements into links by nesting them within an a element.
  <a href="#"><img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="Three kittens running towards the camera."></a>
  
  Unordered list (bullet point style list)
  
  <ul>
  <li>milk</li>
  <li>cheese</li>
</ul>
  
  Ordered lists (numbered lists)
  
  <ol>
  <li>Garfield</li>
  <li>Sylvester</li>
</ol>
  
  Text field - get input from your user, input elements are self-closing.
  
  <input type="text">
  
  Text field with placeholder - Placeholder text is displayed in your input element before your user has inputted anything.
  
  <input type="text" placeholder="this is placeholder text">
  
  Form element - web forms that actually submit data to a server. You can do this by specifying an action attribute on your form element.
  
  <form action="url-where-you-want-to-submit-form-data">
  <input>
</form>
  
  Submit button to a form -  Clicking this button will send the data from your form to the URL you specified with your form's action attribute.
  
  <button type="submit">this button submits the form</button>
  
  You can require specific form fields so that your user will not be able to submit your form until he or she has filled them out.

For example, if you wanted to make a text input field required, you can just add the attribute required within your input element, like this: <input type="text" required>
  
  You can use radio buttons for questions where you want the user to only give you one answer out of multiple options
  Radio buttons are a type of input. Each of your radio buttons can be nested within its own label element. By wrapping an input element inside of a label element it will automatically associate the radio button input with the label element surrounding it. All related radio buttons should have the same name attribute to create a radio button group. By creating a radio group, selecting any single radio button will automatically deselect the other buttons within the same group ensuring only one answer is provided by the user.
  
   <label> 
  <input type="radio" name="indoor-outdoor">Indoor 
</label>
  
  It is considered best practice to set a for attribute on the label element, with a value that matches the value of the id attribute of the input element. This allows assistive technologies to create a linked relationship between the label and the related input element.
  
  <input id="indoor" type="radio" name="indoor-outdoor">
<label for="indoor">Indoor</label>
  
  We can also nest the input element within the label tags:
  
  <label for="indoor"> 
  <input id="indoor" type="radio" name="indoor-outdoor">Indoor 
</label>
  
  Forms commonly use checkboxes for questions that may have more than one answer. Checkboxes are a type of input.
  
  Rules are the same as for radio buttons.
  
  <label for="loving"><input id="loving" type="checkbox" name="personality"> Loving</label>
  
  When a form gets submitted, the data is sent to the server and includes entries for the options selected. Inputs of type radio and checkbox report their values from the value attribute.
  
  <label for="indoor">
  <input id="indoor" value="indoor" type="radio" name="indoor-outdoor">Indoor
</label>
<label for="outdoor">
  <input id="outdoor" value="outdoor" type="radio" name="indoor-outdoor">Outdoor
</label>
  
  If you omit the value attribute, the submitted form data uses the default value, which is on. In this scenario, if the user clicked the "indoor" option and submitted the form, the resulting form data would be indoor-outdoor=on, which is not useful. So the value attribute needs to be set to something to identify the option.
  
  You can set a checkbox or radio button to be checked by default using the checked attribute.
  
  <input type="radio" name="test-name" checked>
  
  The div element, also known as a division element, is a general purpose container for other elements.

The div element is probably the most commonly used HTML element of all.
  
  At the top of your document, you need to tell the browser which version of HTML your page is using.  Most major browsers support the latest specification, which is HTML5. <!DOCTYPE html>.
  
  The ! and uppercase DOCTYPE is important, especially for older browsers. The html is not case sensitive.
  
  The rest of your HTML code needs to be wrapped in html tags
  
  <!DOCTYPE html>
<html>

</html>
  
  You can add another level of organization in your HTML document within the html tags with the head and body elements. Any markup with information about your page would go into the head tag. Then any markup with the content of the page (what displays for a user) would go into the body tag.

Metadata elements, such as link, meta, title, and style, typically go inside the head element.
  
  <!DOCTYPE html>
<html>
  <head>
    <meta />
  </head>
  <body>
    <div>
    </div>
  </body>
</html>
  
</details>

<details><summary>CSS</summary>
  
CSS, or Cascading Style Sheets, tell the browser how to display the text and other content that you write in HTML. With CSS, you can control the color, font, size, spacing, and many other aspects of HTML elements.
  
  We can do this by changing the style of your h2 element.
  
  color style property - change text color
  
  <h2 style="color: blue;">CatPhotoApp</h2>
  
  It is a good practice to end inline style declarations with a ; .
  
  <h2 style="color: red;">CatPhotoApp</h2> - styling that individual h2 element with inline CSS, which stands for Cascading Style Sheets.
  
  there's a better way to apply CSS. style block
  
  <style>
</style>
  
  Inside that style block, you can create a CSS selector for all h2 elements adding style definition with style rules.
  
  <style>
  h2 {
    color: red;
  }
</style>
  
  Classes are reusable styles that can be added to HTML elements.
  
  <style>
  .blue-text {
    color: blue;
  }
</style>
  
  You can apply a class to an HTML element like this: <h2 class="blue-text">CatPhotoApp</h2>.
  In your HTML elements' class attribute, the class name does not include the period.
  Classes allow you to use the same CSS styles on multiple HTML elements.
  
  
  Font size is controlled by the font-size CSS property, like this:
  
  h1 {
  font-size: 30px;
}
  
  You can set which font an element should use, by using the font-family property.
  
  h2 {
  font-family: sans-serif;
}
  
  In addition to specifying common fonts that are found on most operating systems, we can also specify non-standard, custom web fonts for use on our website.
  Google Fonts is a free library of web fonts that you can use in your CSS by referencing the font's URL.
  
  <link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
  
  Now you can use the Lobster font in your CSS by using Lobster as the FAMILY_NAME as in the following example:
  
  font-family: FAMILY_NAME, GENERIC_NAME;
  
  The GENERIC_NAME is optional, and is a fallback font in case the other specified font is not available.
  
  Family names are case-sensitive and need to be wrapped in quotes if there is a space in the name. You need quotes to use the "Open Sans" font, but not to use the Lobster font.
  
  There are several default fonts that are available in all browsers. These generic font families include monospace, serif and sans-serif.
  
  When one font isn't available, you can tell the browser to "degrade" to another font.

  p {
  font-family: Helvetica, sans-serif;
}
  
  Generic font family names are not case-sensitive. Also, they do not need quotes because they are CSS keywords.
  
CSS has a property called width that controls an element's width. Just like with fonts, we'll use px (pixels) to specify the image's width.
  
  <style>
  .larger-image {
    width: 500px;
  }
</style>
  
  CSS borders have properties like style, color and width.
  
  <style>
  .thin-red-border {
    border-color: red;
    border-width: 5px;
    border-style: solid;
  }
</style>
  
   you can apply multiple classes to an element using its class attribute, by separating each class name with a space. 
  
  <img class="class1 class2">
  
  We can round out those corners with a CSS property called border-radius. You can specify a border-radius with pixels.
  In addition to pixels, you can also specify the border-radius using a percentage.
  
  You can set an element's background color with the background-color property.
  
  .green-background {
  background-color: green;
}
  
  In addition to classes, each HTML element can also have an id attribute.
  
   You can use an id to style a single element and you can use them to select and modify specific elements with JavaScript.
  id attributes should be unique. Browsers won't enforce this, but it is a widely agreed upon best practice.
  
  <h2 id="cat-photo-app">
  
  id attributes is that, like classes, you can style them using CSS.

However, an id is not reusable and should only be applied to one element. An id also has a higher specificity (importance) than a class so if both are applied to the same element and have conflicting styles, the styles of the id will be applied.
  
  #cat-photo-element {
  background-color: green;
}
  
  Note that inside your style element, you always reference classes by putting a . in front of their names. You always reference ids by putting a # in front of their names.
  
    All HTML elements are essentially little rectangles. Three important properties control the space that surrounds each HTML element: padding, border, and margin. An element's padding controls the amount of space between the element's content and its border.
    
    An element's margin controls the amount of space between an element's border and surrounding elements. If you set an element's margin to a negative value, the element will grow larger.
     
    CSS allows you to control the padding of all four individual sides of an element with the padding-top, padding-right, padding-bottom, and padding-left properties.
    
    or padding: 10px 20px 10px 20px; - These four values work like a clock: top, right, bottom, left

CSS allows you to control the margin of all four individual sides of an element with the margin-top, margin-right, margin-bottom, and margin-left properties.
    
    or margin: 10px 20px 10px 20px; - These four values work like a clock: top, right, bottom, left
    
    
    You have been adding id or class attributes to elements that you wish to specifically style. These are known as ID and class selectors. There are other CSS Selectors you can use to select custom groups of elements to style.
    
  [attr=value] attribute selector to style the checkboxes - This selector matches and styles elements with a specific attribute value.
    
    [type='radio'] {
  margin: 20px 0px 20px 0px;
}
    
Pixels are a type of length unit, which is what tells the browser how to size or space an item. In addition to px, CSS has a number of different length unit options that you can use.    
    
The two main types of length units are absolute and relative. Absolute units tie to physical units of length. For example, in and mm refer to inches and millimeters, respectively. Absolute length units approximate the actual measurement on a screen, but there are some differences depending on a screen's resolution.    
    
 Relative units, such as em or rem, are relative to another length value. For example, em is based on the size of an element's font. If you use it to set the font-size property itself, it's relative to the parent's font-size.   
    
There are several relative unit options that are tied to the size of the viewport.   
    
    Every HTML page has a body element.
    
    body {
  background-color: black;
}
    
    Remember, you can style your body element just like any other HTML element, and all your other elements will inherit your body element's styles.
    
    Sometimes your HTML elements will receive multiple styles that conflict with one another.
    
    We just proved that our classes will override the body element's CSS.
    
    
    Applying multiple class attributes to a HTML element is done with a space between them like this:

class="class1 class2"
Note: It doesn't matter which order the classes are listed in the HTML element.
    
   However, the order of the class declarations in the <style> section is what is important. The second declaration will always take precedence over the first. 
    
    We just proved that browsers read CSS from top to bottom in order of their declaration. That means that, in the event of a conflict, the browser will use whichever CSS declaration came last.
    
    Note: It doesn't matter whether you declare this CSS above or below pink-text class, since the id attribute will always take precedence. So we've proven that id declarations override class declarations, regardless of where they are declared in your style element CSS.
    
    We just proved that inline styles will override all the CSS declarations in your style element.
    
 In many situations, you will use CSS libraries. These may accidentally override your own CSS. So when you absolutely need to be sure that an element has specific CSS, you can use !important.   
    
    color: red !important;
    
   We usually use decimals, or base 10 numbers, which use the symbols 0 to 9 for each digit. Hexadecimals (or hex) are base 16 numbers. This means it uses sixteen distinct symbols. Like decimals, the symbols 0-9 represent the values zero to nine. Then A,B,C,D,E,F represent the values ten to fifteen. Altogether, 0 to F can represent a digit in hexadecimal, giving us 16 total possible values. 
    
    In CSS, we can use 6 hexadecimal digits to represent colors, two each for the red (R), green (G), and blue (B) components. For example, #000000 is black and is also the lowest possible value.
    
    body {
  color: #000000;
}
    
    From these three pure colors (red, green, and blue), we can vary the amounts of each to create over 16 million other colors!
    
    The digit 0 is the lowest number in hex code, and represents a complete absence of color.

The digit F is the highest number in hex code, and represents the maximum possible brightness.
    
    
    Dodger Blue	#1E90FF
Green	#00FF00
Orange	#FFA500
Red	#FF0000
    
    Many people feel overwhelmed by the possibilities of more than 16 million colors. And it's difficult to remember hex code. Fortunately, you can shorten it.
    
    For example, red's hex code #FF0000 can be shortened to #F00. This shortened form gives one digit for red, one digit for green, and one digit for blue.

This reduces the total number of possible colors to around 4,000. But browsers will interpret #FF0000 and #F00 as exactly the same color.
    
    Another way you can represent colors in CSS is by using RGB values.
    
    Instead of using six hexadecimal digits like you do with hex code, with RGB you specify the brightness of each color with a number between 0 and 255.

If you do the math, the two digits for one color equal 16 times 16, which gives us 256 total values. So RGB, which starts counting from zero, has the exact same number of possible values as hex code.
    
    
    
    body {
  background-color: rgb(255, 165, 0);
}
    
    Just like with hex code, you can mix colors in RGB by using combinations of different values.
    
    CSS Variables are a powerful way to change many CSS style properties at once by changing only one value.
    --penguin-skin: black;
    background: var(--penguin-skin, gray);
    
    
    
    To create a CSS variable, you just need to give it a name with two hyphens in front of it and assign it a value like this:

--penguin-skin: gray;
This will create a variable named --penguin-skin and assign it the value of gray. Now you can use that variable elsewhere in your CSS to change the value of other properties to gray.
    
    After you create your variable, you can assign its value to other CSS properties by referencing the name you gave it.
    
    background: var(--penguin-skin);
    
    Note that styles will not be applied unless the variable names are an exact match.
    
    When using your variable as a CSS property value, you can attach a fallback value that your browser will revert to if the given variable is invalid.
    
    Note: This fallback is not used to increase browser compatibility, and it will not work on IE browsers. Rather, it is used so that the browser has a color to display if it cannot find your variable.
    
    background: var(--penguin-skin, black);
    
    This will set background to black if your variable wasn't set. Note that this can be useful for debugging.
    
    When working with CSS you will likely run into browser compatibility issues at some point. This is why it's important to provide browser fallbacks to avoid potential problems.

When your browser parses the CSS of a webpage, it ignores any properties that it doesn't recognize or support. For example, if you use a CSS variable to assign a background color on a site, Internet Explorer will ignore the background color because it does not support CSS variables. In that case, the browser will use whatever value it has for that property. If it can't find any other value set for that property, it will revert to the default value, which is typically not ideal.

This means that if you do want to provide a browser fallback, it's as easy as providing another more widely supported value immediately before your declaration. That way an older browser will have something to fall back on, while a newer browser will just interpret whatever declaration comes later in the cascade.
    
    When you create a variable, it is available for you to use inside the selector in which you create it. It also is available in any of that selector's descendants. This happens because CSS variables are inherited, just like ordinary properties.

To make use of inheritance, CSS variables are often defined in the :root element.

:root is a pseudo-class selector that matches the root element of the document, usually the html element. By creating your variables in :root, they will be available globally and can be accessed from any other selector in the style sheet.
    
    When you create your variables in :root they will set the value of that variable for the whole page.

You can then over-write these variables by setting them again within a specific selector.
    
    CSS Variables can simplify the way you use media queries.

For instance, when your screen is smaller or larger than your media query break point, you can change the value of a variable, and it will apply its style wherever it is used.
    
    Visual design is a combination of typography, color theory, graphics, animation, page layout, and more to help deliver your unique message.
    
</details>

<details><summary>JavaScript</summary>
  

  
</details>


