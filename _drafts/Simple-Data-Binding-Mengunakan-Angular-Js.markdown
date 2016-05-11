---
layout: post
title : "Simple Data Binding Menggunakan Angular.Js"
date: 2015-11-14 14:27:00
author: "Andy Marthin"
comments:  true
header-img: "img/angularjsgoogle.png"
categories:
- javascript
---

Angular.Js merupakan  front-end framework javascript yang dikembangkan oleh Google.

Index.html

```html
<!DOCTYPE html>
<html lang="en" ng-app="emailApp">
<head>
	<meta charset="UTF-8">
	<title>Simple Binding Menggunakan Angular.js</title>
	<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.3.15/angular.min.js"></script>
	<script src="app.js"></script>
</head>
<body  >
	<input type="text" ng-model="nama">
	<p>Halo { { nama } }</p>
	<br>
	<div ng-controller="EmailListController as emailList">
		<h2>Email</h2>
		<input type="text" ng-model="emailList.emailText" >
		<button ng-click="emailList.addEmail()" >+</button>
	<div>
		Daftar Email:
		<ul>
			<li ng-repeat="email in emailList.emails">{{email.text}}</li>
		</ul>
	</div>
	</div>
</body>
</html>
```

App.js
{% highlight javascript linenos %}
angular.module('emailApp', [])
	.controller('EmailListController', function () {
		var emailList = this;
		emailList.emails = [
			{text: 'andy@marthin.web.id'}];

		emailList.addEmail = function(){
			emailList.emails.push({text:emailList.emailText});
			emailList.emailText = "";
		};
	});

{% endhighlight %}

![Data Binding Angular]({{ site.url}}/img/Data Binding Angular js.png)
