# Utilisez des API REST dans vos projets web
		link: https://openclassrooms.com/fr/courses/3449001-utilisez-des-api-rest-dans-vos-projets-web

## Qu'est ce qu'une API
Une API (Application programming interface) is a interface that allow you to interract with other application.
You need to look at the document of a API to be able to use it ex: the documentation of paypal (https://developer.paypal.com/docs/api/overview/).
You can also decide to build your own API for your own application. This will allow developer to interact with your application in a controled environment.

## What is REST?

It is a standard. REST stands for "Representational State Transfer". It was created by Roy Fielding.
An API REST is based on http. A client do a request to the server and the server answers. The basic method are GET, PUT, POST, DELETE, etc.
To be a RESTful API, the API needs to be:
	- without state.(the server doesn't know the state of the client in between to requests).
	- Cacheable.(a client needs to be able to put data in the cache to reduce the amount of request).
	- client-server oriented.
	- with a uniform interface.
	- with a layer system.
	- code upon request.
A REST API can send JSON, XML, CSV, RSS files.

It exists also SOAP API, for 'simple Object Access Protocol'.
