# Create Azure App Service
[Back to Main](README.md)

This tutorial walks through building an Azure App Service and then synchronizing the app created in the [Basic API Tutorial](BuildAPI.md) to it.

From the Azure Portal, search for "App Services" and then create a new one.  You'll want to ensure you have an Azure subscription and a Resource Group for this.
The name of your App Service must be globally unique.  Below is an example:

![image](https://user-images.githubusercontent.com/16612216/148632536-85676ab4-6881-44dc-a967-10ebc203c0ab.png)

On the Deployment tab, leave the defaults.

On the Monitoring tab, leave the Application Insights defaults (it will create a new instance for this, that's fine).

Click Review+Create and then Create.  If you've filled out all the required fields properly on the Basic tab, the deployment should only take a minute or two.

Once complete, click "Go To Resource" and you'll be taken to the overview.

![image](https://user-images.githubusercontent.com/16612216/148632592-12183dd2-01dc-4e30-bf6e-a12caaa4c7ef.png)

You'll see the URL of your new App Service in the upper right.  If you browse there, you should see the following.  If so, then you've created
the App Service properly and we can move on to synchronizing the vehicle API.

![image](https://user-images.githubusercontent.com/16612216/148632611-baa1047f-4039-4eb0-a147-c12f7e4e0a7f.png)


## Deploy Code to App Service

With your App Service ready to go, the next step is to synchronize your previously created Web API to it.

From VS Code, open the command bar (CTRL+SHIFT+P) and search for `Azure App Service: Deploy to Web App` and click on it

![image](https://user-images.githubusercontent.com/16612216/148632672-635e5ef2-d5c6-4a24-b5ea-cc7ffb2b2059.png)

The first question it asks is what folder to deploy, so select our sample:

![image](https://user-images.githubusercontent.com/16612216/148632686-78268453-d2af-4f7b-a1aa-db0fde036dc7.png)

You may get the following message:

![image](https://user-images.githubusercontent.com/16612216/148632697-5310eacd-3559-4a13-9b50-16f56f908813.png)

This is normal - you'll then be asked to sign into Azure:

![image](https://user-images.githubusercontent.com/16612216/148632702-ba590fdd-eb0a-457c-8c97-086e4fc63932.png)

Perform the authentication and the next question it asks is to select the subscription.  Pick the correct subscription and then
it asks for the Web App.  Select the one you created above:

![image](https://user-images.githubusercontent.com/16612216/148632760-fd7effa8-7034-46b2-9216-eb11465ca546.png)

You'll get a pop up asking if you're sure you want to deploy.  This will overwrite any existing code in the App Service.
Since this is the first time we're deploying, and we want to overwrite what's there, click 'Deploy'.

After a few seconds your deployment should complete successfully (view from the Output tab in VS Code):

![image](https://user-images.githubusercontent.com/16612216/148632809-17533a4f-1935-44eb-ae00-9d4c843ceb19.png)

To test this, navigate to your App Services URL (found in the App Services overview page) and you should see the API you built:

![image](https://user-images.githubusercontent.com/16612216/148632839-584ef904-50cb-4da0-b74c-f39c5fbb1490.png)

This time, instead of being run from localhost, it's hosted now in Azure!

[Back to Main](README.md)
