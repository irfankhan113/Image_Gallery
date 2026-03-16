# Ex.07 Design of Interactive Image Gallery

## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM
gallery.html
```
{% load static %}
<!DOCTYPE html>
<html>
<head>
<title>Luxury Watch Collection</title>

<style>

body{
margin:0;
background:#0d0d0d;
font-family: Arial, Helvetica, sans-serif;
color:white;
text-align:center;
}

h1{
margin-top:30px;
letter-spacing:4px;
color:#d4af37;
}

.gallery{
width:90%;
margin:auto;
margin-top:40px;
display:grid;
grid-template-columns: repeat(5,1fr);
gap:20px;
}

.watch-card{
background:#1c1c1c;
border-radius:12px;
padding:10px;
cursor:pointer;
transition:0.3s;
}

.watch-card:hover{
transform:scale(1.05);
box-shadow:0px 5px 15px rgba(0,0,0,0.7);
}

.watch-card img{
width:100%;
border-radius:10px;
}

.watch-name{
margin-top:8px;
font-size:14px;
color:#d4af37;
}

.viewer{
display:none;
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,0.9);
justify-content:center;
align-items:center;
}

.viewer img{
width:500px;
border-radius:10px;
}

.close-btn{
position:absolute;
top:20px;
right:40px;
font-size:35px;
cursor:pointer;
color:white;
}

</style>

</head>

<body>

<h1>LUXURY WATCH COLLECTION</h1>

<div class="gallery">

<div class="watch-card">
<img src="{% static 'img/image5.jpg' %}" onclick="openImage(this.src)">
<div class="watch-name">Rolex Submariner</div>
</div>

<div class="watch-card">
<img src="{% static 'img/image1.jpg' %}" onclick="openImage(this.src)">
<div class="watch-name">Omega Seamaster</div>
</div>

<div class="watch-card">
<img src="{% static 'img/image2.jpg' %}" onclick="openImage(this.src)">
<div class="watch-name">Tag Heuer Carrera</div>
</div>

<div class="watch-card">
<img src="{% static 'img/image3.jpg' %}" onclick="openImage(this.src)">
<div class="watch-name">Patek Philippe</div>
</div>

<div class="watch-card">
<img src="{% static 'img/image4.jpg' %}" onclick="openImage(this.src)">
<div class="watch-name">Audemars Piguet</div>
</div>

</div>

<div class="viewer" id="overlay">
<span class="close-btn" onclick="closeImage()">×</span>
<img id="largeImage">
</div>

<script>

function openImage(src){
document.getElementById("largeImage").src = src;
document.getElementById("overlay").style.display = "flex";
}

function closeImage(){
document.getElementById("overlay").style.display = "none";
}

</script>

</body>
</html>

```


## OUTPUT

![](<Screenshot 2026-03-16 054305.png>) 
![](<Screenshot 2026-03-16 054355.png>) 
![](<Screenshot 2026-03-16 054419.png>) 
![](<Screenshot 2026-03-16 054444.png>) 
![](<Screenshot 2026-03-16 054505.png>) 
![](<Screenshot 2026-03-16 054525.png>)

## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
