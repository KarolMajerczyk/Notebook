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
  
  
  
  
  
  
  
  
  
  
  
  

</details>

<details><summary>JavaScript</summary>

</details>


