# DOM-and-some-Element-Selectors
## DOM - DOCUMENT OBJECT MODEL
- An object that represents the page you in the web browswer which provides you with an API to interact with it.
- Web Browser constructs the DOM when it loads an HTML document
- It structures all the elements in a tree like representation
```
    <DOCTYPE html>
    <html lang='en'>
    <head>
      <meta charset='UTF-8'>
      <meta nam='' content=''>
      <title>My Title</title>
      <link>
    </head>
    <body>
      <h1>A Heading</h1>
      <a href="http://" alt=''>Link t</a>
      <script></script>
    </body>
```
<img width="275" height="321" alt="dom" src="https://github.com/user-attachments/assets/74a5f79d-9273-4ee0-a75b-b8ee3bde3e61" />
- Javascript can access the DOM to dynamically change the content, structure, and style of a web page
- Consoling document gives an object with properties
  - console.log(document);
- Like any other object to access the object and its properties we the objects name = document.
- This allows us to dynamically change any properties without css

      console.log(document.title); --> prints My title
- If we change it --> document.title = 'My Website';

      console.log(document.title); --> printes My Website
- Find the document background color

      console.log(document.body.style.backgroundColor); --> prints white
- We can change it with document.body.style.backgroundColor = 'black';

      console.log(document.body.style.backgroundColor); --> prints black
- To access the object properties use dot model.
- Another Example
- A webpage title looks like this:
 
  <img width="151" height="51" alt="welcome" src="https://github.com/user-attachments/assets/a77ec1b4-1178-475d-b888-54f4efd5c997" />
- We can access the title or the h1 element dynamically and conditionally change it.
- First get the h1 element by getting the id of the element
  
    const username = 'Jack';
    const welcoming = document.getElementById('welcome-msg');
    wecomeMsg.textContent += username === "" ? 'Guest' : username;
- Webpage now looks like:

  <img width="202" height="46" alt="welcome jack" src="https://github.com/user-attachments/assets/7a133717-8ae0-4570-9d05-1f3a4cf6f308" />

