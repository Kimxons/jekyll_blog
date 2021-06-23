---
layout: post
title:  "Whatsapp Chatbot in Flask & Twillio"
date:   2021-06-23 07:30:20 +0300
categories: jekyll update
---

A [chatbot]("https://en.wikipedia.org/wiki/Chatbot") is a software application that is used to conduct an on-line conversation with a human user through written or text-to-speech, in lieu of providing direct contact with a live **human agent**.

Let’s explore how we can build a chatbot for WhatsApp using the [Twilio API for WhatsApp]("https://www.twilio.com/whatsapp") and the [Flask framework for Python]("https://www.palletsprojects.com/p/flask/").

#### Requirements..?

1. Python 3.6 or newer. For Linux users, python is installed by default. Otherwise you can download it from [python]("http://python.org")

2. Ngrok. This helps you connect the flask application running in your machine to a public URL that twilio can connect to. You can get it at [ngrok]("https://ngrok.com/download")

3. Flask. This is a micro-framework for python. It will help us create a web app that responds to incoming WhatsApp messages. [Flask]("https://flask.palletsprojects.com/en/1.1.x/installation/#install-flask")

4. Create a Twilio account.

5. A WhatsApp enabled smartphone.

#### Setting up your Testing Sandbox

Twilio provides a [WhatsApp Sandbox]("https://www.twilio.com/login?g=%2Fconsole%2Fsms%2Fwhatsapp%2Flearn%3F&t=f8ac1360bcde721e2e5d56ee98dc6b802a45b3aaa9b8b32b418cb431010b9d60") where you can easily develop and test your web app.

To connect your smartphone to the sandbox, from your Twilio console, select Programmable sms and then click WhatsApp. The WhatsApp sandbox page displays the sandbox number assigned to your account and a join code.

To enable the WhatsApp sandbox for your smartphone, send a WhatsApp text with the given code to the sandbox number assigned. You should receive a text from twilio indicating that your mobile number is connected to the sandbox and you can start sending and receiving messages. It’s that simple!

#### Let’s prepare our environment

Open your terminal, create a new directory for  your project and navigate into the directory. Create a virtual environment and activate your environment. Install Twilio and Flask and requests. pip is a python package installer

1. $ mkdir whatsapp-chatbot

2. $ cd whatsapp-chatbot

3. $ virtualenv

4. $ source /bin/activate

5. (name-of-env) $ pip install twilio flask requests

Test whether your installations of flask is working.

	from flask import Flask
	app = Flask(__name__)

	@app.route("/")
	def hello():
	return "Hello World!"

	if __name__ == "__main__":
	app.run(debug=True)

To run 

	python(v) run.py 

#### Let’s create our chatbot,


Let’s code a little bit!

The chatbot will recognize anything that has the word “quote” and respond to it otherwise it will return an error text.

#### Create a Webhook

The Twilio API for WhatsApp uses a webhook to notify an app when there is an incoming text message. Flask makes it easy to create a webhook.

	from flask import Flask
	app = Flask(__name__)
	@app.route("/", methods=["POST"])
	    def index():
	    #add your webhook logic here and return a response
	if __name__=='__main__':
	    app.run()	

We have defined a / endpoint that listens only to POST requests. This endpoint is invoked every time an incoming message from a user is received by Twilio.

The logic defined in our function index() will analyze messages sent by the user and return the appropriate response, in our case, a random quote or an error text.

#### Getting Messages And  Responses

We need to obtain the text send by the user.

	from flask import request
	new_msg = request.values.get('Body', '').lower()

Twilio expects a response in [Twilio Markup Language]("https://www.twilio.com/docs/glossary/what-is-twilio-markup-language-twiml"), which is XML-based.

	from twilio.twiml.messaging_response import MessagingResponse

	resposnse = MessagingResponse()
	msg = response.message()
	msg.boby('some text')

#### Let’s build our chatbot logic

We search the incoming text for the keyword “quote”, then return a response

	responnded = False
	if "quote" in new_msg:
	#quote response
	responded = True
	else:
	#add error message to be displayed
	if not responded:
	#a text to be returned as response

Run your chatbot 

	(name-of-env) $ python app.py

The service is running on your laptop. We need to expose it. To do this, we use ngrok.

Open your terminal and run; Since our app is running on port 5000; Our HTTP requests will be redirected to the temporary domain created.

	ngrok http 5000

On the Twilio console, click Programmable SMS, then WhatsApp and then the sandbox. Copy the URL from ngrok output and paste it in the sandbox.

You are good to go. Send messages from your smartphone and enjoy!!

You can find all the code for this article on: [Chatbot Tutorial code]("https://github.com/Kimxons/whatsapp_chatbot")


Incase of any queries, kindly hit me up on [Twitter]("twitter.com/mishaelkimxons") or [Github]("github.com/kimxons")