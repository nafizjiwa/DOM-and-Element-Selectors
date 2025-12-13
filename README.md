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

      console.log(document);
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

## Element Selectors
- Methods use to target and manipulate HTML elements
- They allow you to select one or multiple HTML elements from the DOM
```
   1. document.getElementById() --> Returns ELEMENT or NULL
   2. document.getElementsByClassName() --> Returns an HTML COLLECTION
   3. document.getElementByTagName() --> Returns an HTML COLLECTION
   4. document.querySelector()    --> Returns the first ELEMENT or NULL(no match)
   5. document.querySelectorAll() --> Returns a NODELIST
        - NODELIST - A COLLECTION OF DOM NODES (like arrays have methods)
```
### Example
#### HTML
```
<h1 id="my-heading">Love Food</h1>

<div class="fruits">Apple</div>
<div class="fruits">Orange</div>
<div class="fruits">Banana</div>

<h4>Root Vegtables</h4>
<ul>
  <li>Beets</li>
  <li>Carrots</li>
  <li>Potatoes</li>
</ul>
<h4>Non-Root Vegtables</h4>
<ul>
  <li>Broccoli</li>
  <li>Celery</li>
  <li>Onions</li>
</ul>
```

##### Web Page Output
<img width="176" height="54" alt="food" src="https://github.com/user-attachments/assets/6a0936b5-4d00-45ae-8f93-ddafe380560e" />

#### Manipulate or Change Elements
###### 1. document.getElementById() --> Returns ELEMENT or NULL
```
const myHeading = document.getElementById('my-heading');
myHeading.style.backgroundColor = "yellow";
myHeading.style.textAlign = 'center';
```
##### Web Page Output
<img width="778" height="97" alt="food" src="https://github.com/user-attachments/assets/0f70b2a4-11e9-48fd-9a56-ee866ff8ad8e" />
</br>
- Console the Element </br>
<img width="177" height="39" alt="console1" src="https://github.com/user-attachments/assets/5ffba90f-3252-4d28-8002-a2a765ae0c0a" /> 
</br>
- Results </br>
<img width="305" height="99" alt="console" src="https://github.com/user-attachments/assets/61f82b55-6a91-466a-b021-501e43c61477" />
</br>
<img width="108" height="40" alt="nul" src="https://github.com/user-attachments/assets/060c9056-32b0-47f0-8ae1-f67284fd3b4b" />
</br>

##### 2. document.getElementsByClassName() --> Returns an HTML COLLECTION
```
const fruits = document.getElementyByClassName("fruits");
console.log(fruits);
```
<img width="191" height="120" alt="collection" src="https://github.com/user-attachments/assets/3bbea536-b9b5-42ac-88b3-36d1e0426620" />

- Change an element
- 
  <img width="243" height="181" alt="fruits" src="https://github.com/user-attachments/assets/f27634e2-1e70-4447-86ef-916f72b8498a" />

```
fruits[0].style.backgroundColor = "yellow";
```
<img width="158" height="189" alt="fruitH" src="https://github.com/user-attachments/assets/1dd37a47-3921-4e49-81c2-a40017ac8446" />

##### 3. document.getElementByTagName() --> Returns an HTML COLLECTION
-Highlight all the h4 elements
```
const h4Elements = document.getElementsByTagName('h4');
for(let h4Element of h4Element){
    h4Element.style.backgroundColor = 'yellow';
}
```
<img width="121" height="235" alt="veg" src="https://github.com/user-attachments/assets/eccb3d5a-8067-466f-935b-9bfab55297a3" />

##### 4. document.querySelector()    --> Returns the first matching ELEMENT or NULL (no match)
###### - Return the first element with class .fruits
```
const element = document.querySelector('.fruits');
element.style.backgroundColor = "yellow";
```
<img width="158" height="189" alt="fruitH" src="https://github.com/user-attachments/assets/e52da488-077a-4743-9eb4-8bfa3a56b909" />

###### - Return the first element of tagName (element ul)
```
const element = document.querySelector('ul');
element.style.backgroundColor = "yellow";
```
<img width="115" height="165" alt="tag" src="https://github.com/user-attachments/assets/a7dc8c19-4ad2-44f5-9bde-a3e6e65fc4e9" />

##### 5. document.querySelectorAll() --> Returns a NODELIST
```
const fruits = document.querySelectorAll(".fruits"); --> A LIST OF NODES WITH CLASS .fruits
===> now have access to each node, so access first node in list
fruits[1].style.background = 'yellow';
```
<img width="74" height="64" alt="orange" src="https://github.com/user-attachments/assets/8d07fb38-c7ae-43f0-b7e7-f9976c273a84" />

```
const foods = document.querySelectorAll("li"); --> A LIST OF NODES OF ALL LIST ELEMENTS
foods[0].style.background = 'yellow';
```
<img width="98" height="174" alt="foods" src="https://github.com/user-attachments/assets/2aa149f1-bb7f-4fae-a2e7-1692549027a2" />


