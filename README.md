# Python3-Adfly-Api
Este fork es suficiente para creacion dinamica de links, pero para la lectura y borrado de estos es necesario actualizar la generacion de los hashes para la comunicacion con la API, por que se quedo en la version 2,es doloroso asi que el borrado es sin usar la API
updated Adfly API support for Python 3
by Mateo Wartelle

# Introduction
Adfly or adf.ly is a URL shortening service that allows users to shorten urls which serve a 5 second ad to the end consumer prior to being redirected to there original intended destination.

I began using Adfly in 2008 with the launch of a website dedicted to the Playstation Portable and Playstation 2 Homebrew development. During this time I was in high school and found my passion for computer science. I had used Adfly to fund the cost of my domains and would go on to use it to fund my community college. 

As I came to terms with many deprecated Python 2 modules, functions and packages this was one I could not see coming to an end. I had decided to bring this API back to life with Python 3 support and an easy to use convert_to_adfly function to make calls to.

# Installing 
```
$ git clone https://github.com/MateoWartelle/Python3-Adfly-Api.git
$ cd Python3-Adfly-Api
```
To install dependencies, run
```
$ pip3 install requirements.txt
```
# Config
You will need to go to https://api.adf.ly and grab your SECRET_KET, PUBLIC_KEY & USER ID.<br> 
These will go inside of the class AdflyApiExample()

```python
class AdflyApiExample():
    BASE_HOST = 'https://api.adf.ly'
    SECRET_KEY = 'YOUR SECRET KEY'
    PUBLIC_KEY = 'YOUR PUBLIC KEY'
    USER_ID = 'YOUR USER ID'
    AUTH_TYPE = dict(basic=1, hmac=2)
```
# Making Calls
```
>>> URLShortened = convert_to_adfly("www.google.com")
>>> print (URLShortended)
http://yoineer.com/43U0
```
