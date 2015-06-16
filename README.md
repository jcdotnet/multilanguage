# multilanguage javascript library (a simple way to make your website multilingual)

This is the library I am creating to make some of my projects multilingual, it will allow you to change the UI text to any language you like to without refreshing the page. 

I will share this library so that you can use it if you like. I will also share as soon as possible a very simple test that uses this library.

How does it work?

We have an array called "strings" that store the texts and their translations in each language. For each text will give them a value to the key "data-text" so we can reference them 
and key for each language defined. Note that you can add as many languages as you need and name them as you like. This would be an example for an English/Spanish website.

var strings = [
    {text: "welcome", en_GB: "Hello world", es_ES: "Hola mundo"},
    {text: "signup", en_GB: "Sign up", es_ES: "Regístrese"},
	...
]

We have also an "errors" array so that we can translate the HTML validation errors. In this case the error values are provided and we only have to set the text for every defined language.

var errors = [
    {error: "required", en_GB: "This field cannot be left blank", es_ES: "Completa este campo"},
	...
]

Once you are familiar with these two arrays you need to follow these five steps: 

STEP 1) Add a reference of this library to your project: 

<script src="js/multilanguage.js"></script>

STEP 2) Add the texts you want to be translated into the "strings" and "errors" array. 

STEP 3) Assign the initial language to the global variable "language". You can also get the browser's default language, checking and converting it if necessary. 

var language = "en_GB"

STEP 4) In your HTML add the attribute "data-text" to the element that contains the text to be translated. For example: <h1 data-text="welcome"></h1>

STEP 5) Call to the function ChangeLanguage passing one of the languages we've defined above as parameter to change the UI language without refreshing the page.

It's that easy!

Author: JC / jcdotnet@hotmail.com

This file has been written in pure javascript so you don't have to reference any other libraries. 