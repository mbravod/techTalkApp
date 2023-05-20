# Guide to setting up Github Actions with Azure.

- You need to have a repository in Github where you have your application.
- You need to have your Azure account configured.
- You need to have an active subscription
- You need to have balance in the account, you can do it with the free account too.
- You need to have instaled Visual Studio Code or a text editor compatible with Azure App Service.
- You need to install Azure App Service into Visual Studio Code

![image](https://github.com/mbravod/techTalkApp/assets/5402955/55bd5ffe-8285-4acb-9c1a-2542e423ecc2)

- Once installed, log in to Azure

![image](https://github.com/mbravod/techTalkApp/assets/5402955/5f37e689-a870-481b-bbd5-c3168ff906e9)

- Once logged in, right click on "App Services" and select "Create new Web App... (Advanced)".

![image](https://github.com/mbravod/techTalkApp/assets/5402955/b83a43e0-0e19-40df-9d44-70ebbc81428b)

- Name your app

![image](https://github.com/mbravod/techTalkApp/assets/5402955/5cd10baa-9358-4ec8-b50a-741ba1f36f79)

- Select or create a new group of resources

![image](https://github.com/mbravod/techTalkApp/assets/5402955/65d49228-8ffc-4f2a-8bd6-56980b600a02)

- Select your application stack

![image](https://github.com/mbravod/techTalkApp/assets/5402955/c4723383-1e99-422a-aee6-b3583e4092d5)

- Select the operating system for your application

![image](https://github.com/mbravod/techTalkApp/assets/5402955/5c8b738a-ce42-429c-a636-d8c2394f4e68)

- Select or create a new service plan for the app

![image](https://github.com/mbravod/techTalkApp/assets/5402955/3ca51e78-a7a0-4441-a474-6c6062f50f01)

- Skip the creation of Application Insights resources

![image](https://github.com/mbravod/techTalkApp/assets/5402955/7c3859ea-a18c-4a39-a77e-a89c5540020f)

- In the popup "Always deploy the workspace 'myAppName' to <app-name>" select "Yes". This way as long as you are in the same workspace, Visual Studio Code will deploy every time to the same App Service.
  
-  Once you have created your application expand the name of your application.
  
  ![image](https://github.com/mbravod/techTalkApp/assets/5402955/1f362c64-0669-4801-85b1-7742ee15bd4b)

-  Select "Application Settings" with right click and select "Add New Setting...".
  
  ![image](https://github.com/mbravod/techTalkApp/assets/5402955/791a40ab-c2bb-4b65-86ea-b7578ccb88cf)

-  Type this name in the popup to set the key "SCM_DO_BUILD_DURING_DEPLOYMENT" and press enter.
-  Type "true" to set the key value. This is done to enable the build at deploy time, which automatically detects the startup script and generates the web.config file.
-  To deploy your application manually select the "Deploy..." icon.
  
  ![image](https://github.com/mbravod/techTalkApp/assets/5402955/0d4f641c-539d-4562-94c7-dbba56a11698)

-  Wait for the process to finish and in the popup you will be able to select "Browse Website" to see your application running.
-  Now that we have the application in Azure, we can see its configuration in the "App Services" section.
  
  ![image](https://github.com/mbravod/techTalkApp/assets/5402955/f1268892-3c64-40b1-9129-2d1e852c61ea)

-  Select the name of our application and in the window that appears select the option "Deployment Center".
  
  ![image](https://github.com/mbravod/techTalkApp/assets/5402955/48ec1690-e766-462e-bced-f3b74295ac8c)

-  Inside we select the repository from which we will be deploying.
  
  ![image](https://github.com/mbravod/techTalkApp/assets/5402955/24608fab-7d70-4996-8196-0721507dd197)

-  We will have to authorize access to our Github account. Then we select the information requested, the organization, the repository and the branch we want to be deployed (it can be any branch we want).
  
  ![image](https://github.com/mbravod/techTalkApp/assets/5402955/ca7f948b-a44e-4650-94e5-ed0ca92be582)

-  In the final section, we must select the stack of our app and the version we are going to work with.
  
  ![image](https://github.com/mbravod/techTalkApp/assets/5402955/be40dfdd-f699-495e-a822-1ff0127eb98d)

-  At the end there will be an option to preview the workflow file which looks like this:
  
  ![image](https://github.com/mbravod/techTalkApp/assets/5402955/f74e6a15-8353-45d0-a4ce-3f3f6af742c0)

-  To make these configurations effective we press the save icon, this will create a new folder where the workflow will be included and our repo will look like this:
  
  ![image](https://github.com/mbravod/techTalkApp/assets/5402955/812f9489-b69a-456a-a0d7-3edd0c109c21)

-  To know that our workflow is working correctly, select the "Actions" section and there we will be able to see the status of our action.
  
  ![image](https://github.com/mbravod/techTalkApp/assets/5402955/8c640cb9-47fc-48fd-899e-bd7edcf22db8)

