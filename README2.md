![image](https://user-images.githubusercontent.com/68961012/88884705-c06d2980-d269-11ea-9623-250678ee2120.png)

# AWSHackcathon 
MADD Technology aims to help ACRA resolve their pain points in the current waiver appeal process. 

# Content Page 
> 1. Prerequisites
> 2. Installation & Set-Up
> 3. Solution

# Prerequisites

Before you begin, ensure you have met the following requirements:

- Fully functional AWS account(QuickSight Service/S3 Bucket Database)
- Registered Business with a valid UEN number 
- Registered Telegram account

# Installation & Set-Up

- Register and created a Dialogflow account (URL: https://cloud.google.com/dialogflow/docs)
- Installed Telegram (URL: https://desktop.telegram.org/)
- Installed UIpath (URL: https://www.uipath.com/fr/start-trial)
- Installed Visual Studio 2019 (URL: https://code.visualstudio.com/download)

# Solution

## Single Portal Submission(ChatBot)

For Single Portal Submission(SPS), An agent will be created in the DialogFlow Console, and various intents will be created according to the required context. Within the created intent, training phases should be inserted, to train the dialog Flow agent in order to capture user's responses. We can also set this response to a binary Click-button option. Following the selection of an option, a Prompt for submission will be created, and once the user clicks on the button, it will direct them to a web server which is directly connected to the database used for processing these appeal cases. System entities(Object identifier) should be created to validate the User's personal details for the appeal submission.

Lastly, the dialog Flow agent will be linked to the telegram platform ChatBot. (Other chatbots can also be link. e.g Facebook messenger, twitter and Viber)

- Step 1: Create a Telegram Bot through @Botfather. 

- Step 2: Copy the generated token number.

- Step 3: Paste the Token number into the dialog Flow Agent through the "integrations" tab.

- Step 4: Enable Fulfillment (Connecting the WebHook)


## Automated Decision Engine(RPA)

For the Automated Decision Engine(ADE), All new cases will be stored in Amazon S3 bucket. When the new cases is submitted, it will trigger the RPA process to start. Acceptable cases (Details fully filled up, with supporting documents) will be routed to officer for review. Non-Acceptable cases will be rejected, and a rejection email will be sent to customer. 

## AI Analytic Dashboard(Amazon Quicksight) 

The AI Analytic Dashboard (Amazon Quicksight) is used by the ACRA officer to assist them in making judgement on appeal cases. The implementation of Amazon Quicksight would help integrate datasets from different places and generate a more meaningful dashboard such as providing a glance view of the applicant's past performance. Different report can be generated to cater for different business need, E.G. drill down report or Department KPI. Relevant Data would be integrated and visualize using chart for the officer to make better and faster decision. 

Charts for example: 

- Average Company Credit Score
- Overview of past Approved and rejected cases
- Past Year Annual Income  by Case Number
- Overview of past Appeal cases processing time and Status 

From the above charts, it helps officers to make a final judgement on whether they should approve the case or reject it.

# Source code for Website 

https://drive.google.com/file/d/1wEwI0J-NpdCOHrJZcdwXWRLyeoosdYZv/view?usp=sharing
