# Build API Management
[Back to Main](README.md)

This page will walk through building an API Management (APIM) instance and link it to the [Web App](BuildAPI.md) created in the prior step.

Start from the Azure Portal - search for "API Management services" and click to create a new one.

![image](https://user-images.githubusercontent.com/16612216/148633055-86e2caec-c392-4a10-9891-60c6f9294d39.png)

On the Monitoring tab, turn on Application Insights and select the previous instance that was created

![image](https://user-images.githubusercontent.com/16612216/148633027-b9a3d0c7-8927-46b1-86ba-7fc9a0f45db0.png)

On the rest of the tabs, leave the defaults.

Click "Review + Create" and then click "Create".

This process can take a while (around 25-30 minutes to complete).

Once complete, click the APIs link and choose to add an API from an App Service.  You can then click browse for your API:

![image](https://user-images.githubusercontent.com/16612216/148633896-8bbd7ef2-6782-4df1-97df-77f60c0902d7.png)

Add in a URL suffix (I used 'vehicle' in the example aboe).

When that's added, click the API in the list, select settings from the top and uncheck the "Subscription required" for our testing.

![image](https://user-images.githubusercontent.com/16612216/148633961-bce5b912-c107-4744-bc8c-d9d384153d5d.png)

Once saved, you should now be able to browse to the URL of the APIM, add hte suffix, and hit your Web API:

![image](https://user-images.githubusercontent.com/16612216/148634005-152e9371-80df-4166-9091-cafa9dcda34f.png)


[Back to Main](README.md)
