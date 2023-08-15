---
layout: page
title: Flask-Mongoengine RESTful API Example
description: Simple API example completed with Flask and MongoDB
img: 
importance: 2
category: work
giscus_comments: false
---

This repository contains the example code for API project, using MongoEngine, Marshmallow with Flask built on Docker.

User account has to be created to use application. Only registered users can add boards, cards and comments. Entities may be deleted by owners only.

    ---
    app/
    ├── requirements.txt
    ├── wsgi.py
    ├── Dockerfile
    └── server
        ├── __init__.py
        ├── database
        │   ├── __init__.py
        │   ├── models.py
        │   └── schemas.py
        └── resources
            ├── __init__.py
            ├── auth.py
            ├── boards.py
            ├── cards.py
            └── comments.py
    ---




<table>
  <tr>
    <th>Method</th>
    <th>Route</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>GET</td>
    <td>/</td>
    <td>Index of application</td>
  </tr>
  <tr>
    <td>POST</td>
    <td>/auth/register</td>
    <td>Register to application</td>
  </tr>
  <tr>
    <td>POST</td>
    <td>/auth/login</td>
    <td>Login to applicaiton</td>
  </tr>
</table>


## API


<table>
  <tr>
    <th>Method</th>
    <th>Route</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>GET</td>
    <td>/boards/</td>
    <td>List of boards</td>
  </tr>
  <tr>
    <td>POST</td>
    <td>/boards/</td>
    <td>Create a new board</td>
  </tr>
  <tr>
    <td>GET</td>
    <td>/boards/{board_id}</td>
    <td>Get board details by ID</td>
  </tr>
  <tr>
    <td>PUT</td>
    <td>/boards/{board_id}</td>
    <td>Update board details by ID</td>
  </tr>
  <tr>
    <td>DELETE</td>
    <td>/boards/{board_id}</td>
    <td>Delete a board by ID</td>
  </tr>
  <tr>
    <td>POST</td>
    <td>/boards/{board_id}/cards/</td>
    <td>Add a new card to board</td>
  </tr>
</table>


### Cards


<table>
  <tr>
    <th>Method</th>
    <th>Route</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>GET</td>
    <td>/cards/{card_id}</td>
    <td>Get card details by ID</td>
  </tr>
  <tr>
    <td>PUT</td>
    <td>/cards/{card_id}</td>
    <td>Update card details by ID</td>
  </tr>
  <tr>
    <td>DELETE</td>
    <td>/cards/{card_id}</td>
    <td>Delete a card by ID</td>
  </tr>
</table>


### Comments

{% raw  %}
```html
<table>
  <tr>
    <th>Method</th>
    <th>Route</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>GET</td>
    <td>/cards/{card_id}/comments/</td>
    <td>List of comments of card</td>
  </tr>
  <tr>
    <td>GET</td>
    <td>/cards/{card_id}/comments/{comment_id}</td>
    <td>Get comment details by ID</td>
  </tr>
    <tr>
    <td>POST</td>
    <td>/cards/{card_id}/comments/</td>
    <td>Add a new comment to card</td>
  </tr>
  <tr>
    <td>PUT</td>
    <td>/cards/{card_id}/comments/{comment_id}</td>
    <td>Update comment details by ID</td>
  </tr>
  <tr>
    <td>DELETE</td>
    <td>/cards/{card_id}/comments/{comment_id}</td>
    <td>Delete a comment by ID</td>
  </tr>
</table>
```
{% endraw  %}
