---
layout: post
title:  "Tablas centradas, utilizando  html"
date:   2020-06-17 16:40:39
categories: cómo se hace
---

  **Negrita**


<html>
<head>
<style>
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
  width: 100%;
  text-align: left;
  padding: 16px;
}

table.center {
  margin-left: auto; 
  margin-right: auto;
}
</style>
</head>
<body>

<h2>Center a Table</h2>
<p>To center a table, set left and right margin to auto:</p>

<table class="center">
  <tr>
    <th>Firstname</th>
    <th>Lastname</th> 
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
  <tr>
    <td>John</td>
    <td>Doe</td>
    <td>80</td>
  </tr>
</table>

</body>
</html>

  **Negrita**
