# ECCafebot-demo
 telegram bot :https://telegram.me/Eccafebot

google site:https://sites.google.com/view/eccafebot/home
All procedure screenshots and screen recording is uploaded in this repository.



Steps to create bot using Azure bot services and deploy them on telegram using azure are explained.

This project uses Azure congnitive services,Azure bot services and Qna maker.

Steps are as follows:

Open Azure portal.

Type Qna maker.

Select Qna maker and select on create there.

Fill the necessary details in form.

Now knowledge base opens.

Fill questions and answers.

save and train.

Test.

Publish.

Then new tab opens ,there click on create bot.

Now bot is created.

We can download source code of it.

Now go to menu,bot services ,Click on bot you have created.

You can find embeded code of bot and secret key in channels.

Using keys and embeded code ,you can deploy it on google sites.

Otherwise After creating bot ,it will ask to deploy it on varoius social platforms.

Select telegram there.

Now go to telegram.

Join Botfather.

type /newbot

copy the access tokens deisplyed in chat.
fill access tokens on azure portal when it asks for it .Then telegram bot is created.

This is how ECCafebot is created and deployed.



In self learning module it is explained as follows:




The Language service's custom question answering feature enables you to quickly create a knowledge base, either by entering question and answer pairs or from an existing document or web page. It can then use some built-in natural language processing capabilities to interpret questions and find appropriate answers.

Open the Azure portal at https://portal.azure.com, signing in with your Microsoft account.

Click the ＋Create a resource button, search for Language service, and create a Language service resource with the following settings: Select Additional Features

Default features: Keep the default features

Custom features: Select custom question answering Click Continue to create your resource.

Subscription: Your Azure subscription

Resource group: Select an existing resource group or create a new one

Name: A unique name for your Language resource

Pricing tier: Standard S

Azure Search location: Any available location

Azure Search pricing tier: Free F (If this tier is not available, select Standard (S))

Legal Terms: Agree

Responsible AI Notice: Agree

 Note

If you have already provisioned a free-tier Azure Cognitive Search resources, your quota may not allow you to create another one. In which case, select a tier other than F.

Click Review and Create and then click Create. Wait for the deployment of the Language service that will support your custom question answering knowledge base.

In a new browser tab, open the Language Studio portal at https://language.azure.com and sign in using the Microsoft account associated with your Azure subscription.

If prompted to choose a Language resource, select the following settings:

Azure Directory: The Azure directory containing your subscription.
Azure subscription: Your Azure subscription.
Language resource: The Language resource you created previously.
If you are not prompted to choose a language resource, it may be because you have multiple Language resources in your subscription; in which case:

On the bar at the top if the page, click the Settings (⚙) button.
On the Settings page, view the Resources tab.
Select the language resource you just created, and click Switch resource.
At the top of the page, click Language Studio to return to the Language Studio home page.
At the top of the Language Studio portal, in the Create new menu, select Custom question answering.

On the Enter basic information page, enter the following details and click Next:

Language resource: choose your language resource.
Azure search resource: choose your Azure search resource.
Name: MargiesTravel
Description: A simple knowledge base
Source language: English
Default answer when no answer is returned: No answer found
On the Review and finish page, click Create project.

You will be taken to the Manage sources page. Click ＋Add source and select URLs.

In the Add URLs box, click + Add URL. Type in the following:

URL name: MargiesKB
URL: https://raw.githubusercontent.com/MicrosoftLearning/AI-900-AIFundamentals/main/data/qna/margies_faq.docx
Classify file structure: Auto-detect Select Add all.
Edit the knowledge base
Your knowledge base is based on the details in the FAQ document and some pre-defined responses. You can add custom question-and-answer pairs to supplement these.

Click Edit knowledge base on the left hand panel. Then click + Add question pair.
In the Questions box, type Hello. Then click + Add alternative phrasing and type Hi.
In the Answer and prompts box, type Hello. Keep the Source: Editorial.
Click Submit. Then at the top of the page click Save changes. You may need to change the size of your window to see the button.
Train and test the knowledge base
Now that you have a knowledge base, you can test it.

At the top of the page, click Test to test your knowledge base.

In the test pane, at the bottom enter the message Hi. The response Hello should be returned.

In the test pane, at the bottom enter the message I want to book a flight. An appropriate response from the FAQ should be returned.

 Note

The response includes a short answer as well as a more verbose answer passage - the answer passage shows the full text in the FAQ document for the closest matched question, while the short answer is intelligently extracted from the passage. You can control whether the short answer is from the response by using the Display short answer checkbox at the top of the test pane.

Try another question, such as How can I cancel a reservation?

When you're done testing the knowledge base, click Test to close the test pane.

Create a bot for the knowledge base
The knowledge base provides a back-end service that client applications can use to answer questions through some sort of user interface. Commonly, these client applications are bots. To make the knowledge base available to a bot, you must publish it as a service that can be accessed over HTTP. You can then use the Azure Bot Service to create and host a bot that uses the knowledge base to answer user questions.

At the left of the Language Studio page, click Deploy knowledge base. Click Deploy.
After the service has been deployed, click Create a Bot. This opens the Azure portal in a new browser tab so you can create a Web App Bot in your Azure subscription.
In the Azure portal, create a Web App Bot with the following settings (most of these will be pre-populated for you):
Bot handle: A unique name for your bot
Subscription: Your Azure subscription
Resource group: The resource group containing your QnA Maker resource
Location: The same location as your QnA Maker service.
Pricing tier: F0
App name: Same as the Bot handle with .azurewebsites.net appended automatically
SDK language: Choose either C# or Node.js
QnA Auth Key: This should automatically be set to the authentication key for your knowledge base
App service plan/location: This should be set automatically to a suitable plan and location
Application Insights: Off
Microsoft App ID and password: Auto create App ID and password.
Wait for your bot to be created (the notification icon at the top right, which looks like a bell, will be animated while you wait). Then in the notification that deployment has completed, click Go to resource (or alternatively, on the home page, click Resource groups, open the resource group where you created the web app bot, and click it.)
In the left-hand pane of your bot look for Settings, click on Test in Web Chat, and wait until the bot displays the message Hello and welcome! (it may take a few seconds to initialize).
Use the test chat interface to ensure your bot answers questions from your knowledge base as expected. For example, try submitting I need to cancel my hotel.



Creating a new custom question answering service
Create a Text Analytics resource to use question answering and other features such as entity recognition, sentiment analysis, etc.

Now when you create a new Text Analytics resource, you can select features that you want included. Select custom question answering (preview) and continue to create your resource.



You can no longer create a QnA Maker managed resource from the QnA Maker create flow, instead you will be redirected to the Text Analytics service. There is no change to the QnA Maker stable release.
Details

All existing QnA Maker managed (preview) resources continue to work as before. There is no action required for these resources at this time.
The creation flow for Custom question answering (preview) is the primary change. The service, portal, endpoints, SDK, etc. remain as before.
Custom question answering (preview) continues to be offered as a free public preview. This feature is only available as part of Text Analytics Standard resources. Do not change your pricing tier for Text Analytics resources to free.
Custom question answering (preview) is available in the following regions:
South Central US
North Europe
Australia East.


# ECCafebot
ECCafebot is chat bot created using Azure bot service and Qna maker .It gives menu to the customers coming to the cafe.

This webchatbot is hosted in google sites.Its hosted at microsoft azure- https://sites.google.com/view/eccafebot/home 

Azure bot services,cognitive services and Qna maker is used for this project.azure bot created and knowledgebase screenshots are included here.

Eccafebot is deployed on telegram with name @Eccafebot

https://telegram.me/Eccafebot

sample Questions : hi                                             answer:hi sir/madam,how can help you?
                   menu                                            |Coffey |30 |
                                                                   |-------|---|
                                                                   |Tea    |30 |
                                                                   |Juice  |50 |
                                                                   |Samosa |60 |
                                                                   |Burger |100|
                                                                   |Sweets |100|
                                                                   |Chats  |50 |
                                                                   |Chips  |120|
                                                                   |Special|150|
                                                                   |Rice   |200|
                    juice                                          Apple  60
                                                                   Orange 50
                                                                   Chicco 50
                                                                   Choco 65
                                                                   Mix fruit 80
                                                                   Grape 50
                                                                   lemon 20    
                   bye                                             Bye ,Have a good day!

![Screenshot (514)](https://user-images.githubusercontent.com/92110686/160904047-9a459f4e-ef20-46cb-a02e-34e1346c4555.png)
![Screenshot (515)](https://user-images.githubusercontent.com/92110686/161277519-c0667aa6-e4d1-43c8-b8b8-5acc20c0afeb.png)
![Screenshot (516)](https://user-images.githubusercontent.com/92110686/161277537-5cfe1cc9-fbee-48ea-bfa9-283e960d692d.png)
![Screenshot (517)](https://user-images.githubusercontent.com/92110686/161277561-1e4a5045-84e8-46a3-962d-c3014c04faab.png)
![Screenshot (518)](https://user-images.githubusercontent.com/92110686/161277570-f7a41966-5d23-4085-ba08-ca02b052bb42.png)
![Screenshot (519)](https://user-images.githubusercontent.com/92110686/161277579-0c4e7d57-aa80-4c7d-8a55-c9ff3cea9b4e.png)
![Screenshot (522)](https://user-images.githubusercontent.com/92110686/161280817-5d1922fe-1326-4f12-9082-988a61830aaf.png)
![Screenshot (523)](https://user-images.githubusercontent.com/92110686/161280834-df8d5184-a831-4d27-b37e-6021a845c2d7.png)
![image](https://user-images.githubusercontent.com/92110686/161278553-b45b761e-c909-4558-813a-1939ee888e33.png)







