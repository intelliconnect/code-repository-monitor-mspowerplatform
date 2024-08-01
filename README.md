**GitHub Code Repository Monitor Using PowerAutomate – Installation Guide and Manual**

This utility provides recurring alerts for commits to a GitHub repository. It serves as a reminder for instances when a commit might be forgotten or overlooked, helping to ensure that code changes are consistently recorded. This utility is developed using Power Automate.

**Why Use Power Automate?**

Many companies rely on Office 365 applications and services for internal communication and collaboration. Power Automate, integrated within Office 365 Suite, eliminates the need for third-party applications. It offers over a thousand connectors and actions. For this utility, we utilize connectors such as HTTP to call GitHub's REST API and SharePoint actions to retrieve items from a list and MS Teams to communicate with programmers and stakeholders. Note that a Power Automate Premium license is required to use HTTP actions. 

**How Does the Scheduled Flow Provide Alerts?**

The Scheduled Flow is a recurring flow in Power Automate that can be scheduled to run at any desired time or frequency throughout the day. The flow first retrieves the repository list from SharePoint. Based on the repository names, it then iterates through each to check for commits. If no commits are found for the day, it posts a message to MS Teams. 

**How to install this application?**

**Pre-requisite:** Power Automate License

**Step 1**: Download the zip file.

**Step 2:** Go to <https://make.powerautomate.com/> log in with your credentials.

**Step 3:** Go to My Flows.

<img width="81" alt="Picture 1" src="https://github.com/user-attachments/assets/573dcf5c-4add-4505-a106-60d371151b5e">

Here, you will find all your flows.

**Step 4:** Import the zip file which was downloaded earlier

<img width="244" alt="Picture2" src="https://github.com/user-attachments/assets/2c400e7d-88d7-4ff1-8a56-185f06d6e0ba">

Once you select the zip file, it will start importing.

<img width="386" alt="Picture3" src="https://github.com/user-attachments/assets/7b4de84f-fb1a-4697-879f-000b97544635">


**Step 5:** Select the connections required

Click on _Select during import_ and select the connection or create one, it will take a few seconds.

<img width="393" alt="Picture4" src="https://github.com/user-attachments/assets/c5a0f5c9-dc6a-44a3-bd54-246945cfa6a9">

Click on import once you have selected the connections. It will take a minute or two to import, don’t close the window.

**Step 6:** Go to My Flows and Turn on  the flow you just imported

<img width="386" alt="Picture5" src="https://github.com/user-attachments/assets/5780e35d-79f8-4a1b-ad32-150854b413b6">


**Step 7:** Set up the Repository list

Go to the Share Point from application lists. Select the Share Point site, where you can add the list.

<img width="184" alt="Picture6" src="https://github.com/user-attachments/assets/80dcf6c2-3026-438c-a85a-c11980b79fb0"> 
<img width="270" alt="Picture7" src="https://github.com/user-attachments/assets/d60be5df-5654-4110-8131-89155cf4d8db">


**Step 8:** Create a Blank list from Share Point

<img width="437" alt="Picture8" src="https://github.com/user-attachments/assets/1d67d88d-2239-46a2-bd79-75f2f2e03088">

Add three fields like this and add your GitHub organizations and repositories and the respective group chat name in team.

orgname, reponame, team and description

Note: Every repository you are adding must have access from the account you will run the autoamte flow from. 

<img width="468" alt="Picture9" src="https://github.com/user-attachments/assets/a1f0f1d0-cb2b-48d0-a435-deafbfcd57af">


**Step 9:** Add the Share Point list in the flow

Go to My Flows> Click on edit the flow.

Click on Get Items action and select the site your list is in, and then select the list.

Save the flow once you have added the list. (Ignore the warning for OData query)

<img width="426" alt="Picture10" src="https://github.com/user-attachments/assets/9225ba88-7a5a-4883-a7c2-75d39ccd5e65">


**Step 10:** Change the token in HTTP action

Create a token from GitHub>Settings>Developer’s settings> Personal Access Token.

Make a classic token giving repository permissions and copy the token.

<img width="128" alt="Picture11" src="https://github.com/user-attachments/assets/f2923e53-8daf-415a-b990-39bbe7cd3a69">
<img width="307" alt="Picture12" src="https://github.com/user-attachments/assets/a88ccc57-5fc0-4c65-a0e3-4a7e8924613d">


You will find HTTP in such way:

<img width="388" alt="Picture13" src="https://github.com/user-attachments/assets/7987ecf3-9c22-41d2-916d-909ef314e034">


Paste it in HTTP action in the flow.

<img width="378" alt="Picture14" src="https://github.com/user-attachments/assets/30009075-fb40-40ab-8525-6038e60abe99">

And save it, you are done with setting the flow up.

You can customize a few things such as time and the list name.

You can change the recurring time in schedule action:

<img width="374" alt="Picture15" src="https://github.com/user-attachments/assets/a3670105-d78c-4570-ae5f-45302debd4d1">

Once you are done with customizing the flow, hit save and you are done! You will get alerts to the teams you named in Share Point at the time you selected in schedule action.

**How to test the flow?**

Go to My Flows> Github Commits Alert> Edit.

Then, press the test button.

<img width="468" alt="Picture16" src="https://github.com/user-attachments/assets/70f758aa-cae0-42ac-90d7-34079b8db982">


It will show like this:

<img width="468" alt="Picture17" src="https://github.com/user-attachments/assets/01a30c5a-2e1c-4cd7-aa7d-605f2627c930">


And in the Teams, which you mentioned you’d get alert like this:

<img width="468" alt="Picture18" src="https://github.com/user-attachments/assets/2ddd08c2-2802-4061-a574-c5c49a91ebbc">

Since the test was successful, you can now start using it daily.  

We trust this will streamline your workflow and make things easier for you! 

**Ready to Transform your Business with Automation?** [**Get Started**](https://intelliconnectq.com/low-code-and-automation)
