# Dynamic Website Design for a Manufacturing Company
## AIM:
To design a dynamic website for a chip manufacturing company.

## DESIGN STEPS:
### Step 1: 
Requirement collection.
### Step 2:
Creating the layout using HTML and CSS.
### Step 3:
Updating the sample content.
### Step 4:
Choose the appropriate style and color scheme.
### Step 5:
Validate the layout in various browsers.
### Step 6:
Validate the HTML code.
### Step 7:
Create a database model and migrate the database.
### Step 8:
Retrieve data from database and display it in a dynamic webpage.
### Step 9:
Publish the website in the given URL.

## PROGRAM:

### BASE.HTML:

```
{% load static %}
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Silicon Private Limited</title>
    <link rel="stylesheet" href="{% static 'css/layout.css' %}">
    <link rel = "icon" href ="{% static 'img/chip.jpg' %}" type = "image/x-icon"> 
              
</head>

<body>
    <div class="container">
    <div class="banner">
       SAFZZ Silicon Private Limited.
    </div>
    <div class="menu">
        <div class="menuitem"><a href="/home">Home</a></div> 
        <div class="menuitem"><a href="/products">Products</a></div> 
        <div class="menuitem"><a href="/people">People</a></div>
        <div class="menuitem"><a href="/contactus">Contact Us</a></div> 
    </div><div class="content">
    {% block content %}    
    {% endblock  %}
    </div>
    <div class="footer">
        Copyright © 2020 SAFZZ Silicon Private Limited, Developed by SAFA
    </div>
    </div>
</body>

</html>

```

### HOME.HTML:

```
{% extends "companyapp/base.html" %}

{% block content %}
    <div class="homecontent">    
    <h1>About Us</h1>
    <img src="/static/img/building.jpg" alt="Building">
    <div class="contenttext">
    Silicon Pvt Ltd, provides a broad range of semiconductor and infrastructure software applications that serve the data center, networking, software, broadband, wireless, and storage and industrial markets. Common applications for its products include: data center networking, home connectivity, broadband access, telecommunications equipment, smartphones, base stations, data center servers and storage, factory automation, power generation and alternative energy systems, displays, and mainframe operations and management, and application software development. Some of Silicon's core technologies and products include:
    <ul>
        <li>Memory Chips</li>
        <li>SATA HDD</li>
        <li>SATA SSD </li>
        <li>Broadband Modems</li>
        <li>Wifi Devices</li>
        <li>Switching Devices</li>
        <li>Optical Sensors</li>
    </ul> 
    </div>
    </div>
{% endblock  %}

```
### PEOPLE.HTML:

```
{% extends "companyapp/base.html" %}
{% load static %}
<!DOCTYPE html>
<html>

<head>
    <title>PEOPLE LIST</title>
    <link rel="stylesheet" href="{% static 'css/layout.css' %}">
</head>

<body>
    {% block content %}
    <div class="container">
        <h1>OUR CREW</h1>
        <div class="content">
            <div class="peoplelist">
                {% for people in peoples %}
                <div class="people">
                    <div class="peoplelist">
                        <img src="{{ people.photo.url }}" alt="people image">
                    </div>
                    <div class="peoplephoto">{{ photo }}</div>
                    <div class="peoplename">{{ people.name }}</div>
                    <div class="peopledesignation">{{ people.designation }}</div>
                </div>
                {% endfor %}
            </div>
       </div>
    {% endblock %}
    </div>
</body>

</html>

```
### PRODUCTS.HTML:

```
{% extends "companyapp/base.html" %}
{% load static %}
<!DOCTYPE html>
<html>

<head>
    <title>PRODUCTS LIST</title>
    <link rel="stylesheet" href="{% static 'css/layout.css' %}">
</head>

<body>
    {% block content %}
    <div class="container">
        <h1>OUR PREMIUM PRODUCTS</h1>
        <div class="content">
            <div class="peoplelist">
                {% for product in products %}
                <div class="people">
                    <div class="peoplelist">
                        <img src="{{ product.photo.url }}" alt="product image">
                    </div>
                    <div class="peoplephoto">{{ photo }}</div>
                    <div class="peoplename">{{ product.name }}</div>
                    <div class="peopledesignation">{{ product.price }}</div>
                </div>
                {% endfor %}
            </div>
        </div>
    </div>
    {% endblock %}
</body>

</html>

```

### CONTACTUS.HTML:

```
{% extends "companyapp/base.html" %}

{% block content %}
<div class="contactcontent"> 
<h1> CONTACT US </h1>
<h2>ADDRESS :  
       Block -E, First Floor 100 Feet,<br>   Jawaharlal Nehru Rd,<br> Vadapalani,<br> Chennai, Tamil Nadu 600026</h2>
<h2>EMAIL :  safasiraj006@gmail.com</h2>
<h2>Phone :   9962102129</h2>
</div>
{% endblock  %} 

```

## ADMIN PAGE:
![output](./static/img/O6.png)
![output](./static/img/O7.png)

## TEMPLATE CODE:
![output](./static/img/O8.png)
![output](./static/img/O9.png)


## OUTPUT:

![output](./static/img/O1.png)
![output](./static/img/O2.png)
![output](./static/img/O3.png)
![output](./static/img/O4.png)
![output](./static/img/O5.png)


## CODE VALIDATION REPORT:
![output](./static/img/v1.png)
![output](./static/img/v2.png)
![output](./static/img/v3.png)
![output](./static/img/v4.png)



## RESULT:
Thus a website is designed for the chip manufacturing company and is hosted in the URL http://safa.student.saveetha.in:8000/home. HTML code is validated.