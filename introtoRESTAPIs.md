# Introduction to REST APIs
This document contains notes based on the topic [Introduction to REST APIs](https://idratherbewriting.com/learnapidoc/docapis_intro_to_rest_api_doc.html)

## What is an API
- An **API** (or **Application Programming Interface**) provides an interface between two systems.
- APIs are often _pulling_ and _pushing_ data underneath user interfaces.

### Web services
All APIs that use **HTTP** protocol as the transport format for requests and responses are considered web services.
- Web-based application that provides resources in a format consumable by other computers
- Include various types of APIs, including both **REST** and **SOAP** APIs
- Basically _request-and-response_ interactions between **clients** and **servers** (a computer requests a resource, and the web service responds to the request).
- Web services are language-agnostic

<img src="image/restAPImodel.svg" width="800" height="500">

## SOAP (Simple Object Access Protocol) APIs
- _Predecessor_ to REST APIs
- Standardized protocol that requires **XML as the message format** for requests and responses
- Message format is defined through **WSDL** (Web Services Description Language) file
- Messages are enclosed in an **envelope** that includes a **header** and **body**, using a _specific XML schema_ and _namespace_.
- The _main problem_ with SOAP is that the XML message format is too **verbose** and **heavy**.
