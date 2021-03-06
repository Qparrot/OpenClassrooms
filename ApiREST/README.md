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

## Example of API

- Github: https://developer.github.com/. 
- Weather underground: 
- IBM Speech to Text: https://cloud.ibm.com/

Let's us IBM speech to text to learn about API. Search for "Speech to text".
Click on "Create" to activate this service. then on "Service Credentials".
You NEED TO use this Tutorial: https://cloud.ibm.com/docs/services/speech-to-text?topic=speech-to-text-gettingStarted#getting-started-tutorial.

curl -X POST -u "apikey:{apikey}" \
--header "Content-Type: audio/flac" \
--data-binary @/home/quentin/Downloads/audio-file.flac \
"{url}/v1/recognize"

change apikey and {url} {apikey} by the data provided by IBM.

curl -X POST -u "apikey:{apikey} \
--header "Content-Type: application/json" \
--data "{\"text":\" The IBM® Text to Speech service provides an Application Programming Interface (API) that uses IBM's speech-synthesis capabilities to convert text to an audio signal. The service provides a Representational State Transfer (REST) interface that lets you synthesize written text into natural-sounding speech in a variety of languages, accents, and voices. The service currently synthesizes text from English, French, German, Italian, Japanese, Spanish, or Brazilian Portuguese into audio spoken in a male or female voice (the service supports only a single gender for some languages).\"}" \
--output text.wav \
"{url}/v1/synthesize" 

Use this links: https://cloud.ibm.com/docs/services/text-to-speech?topic=text-to-speech-gettingStarted#getting-started-tutorial

Apikey/couple credentials is the right thing to use: https://medium.com/@MissAmaraKay/watson-services-username-password-vs-api-key-1806698316be

## Ressources

Les ressources sont le coeur de l'api. c'est ce que le client vient chercher et ce aue le serveur renvoie. Les API sont basee sur un systeme d'URI(pour Uniform Resource Identifier). A URI is a string of characters that unambiguously identifies a particular resource. It follows a particular hierarchy defined with syntax rules.

You can asks for a set a data: "/users" (it will give you all the users) or a specific data "/users/231" (it will give you the data of the user 231). 
Users is a first level resource.

## The request structure
We can have multiple part in a request:
- The first line includes a VERB(that describes the action to do) a file(that will be taken by the server).
and the HTTP version.
	ex: VERB /file_path.html HTTP/X.X
- the Header can contain the date, the referer, the user agent(the browser), the user language and the cookies
- The Body: it contains the attributes of the request.

## Main Request VERB

GET : you get the data
POST: You ask to add a object to the data
PUT: You ask to add a object at a particular point of the data set.
DELETE: you delete the data.

## The response

The response is divided into 5 chunks:


|| The HTTP VERSION || THE HTTP CODE(404, 200, etc) ||
|| HEADER ||
    ...
|| HEADER ||
|| BODY(the resources)||

## The HTTP CODE

2XX = success
3XX = redirection
4XX = Mistake from the client
5XX = Mistake from the server  

## External services

Apigee = service to do request api. You often need to be identifies
Postman = Service to do api request all over the web.




