# Building a local .NET API.
This tutorial walks you through building a local API with basic GET functionality.  The goal is not to build a useful API, but rather a base API that responds to simple GET queries to be used as a building block for testing APIM.

From VS code, run the following in the terminal to build a basic webapp named "vehicle":

`dotnet new webapi -minimal -o vehicle`

troubleshooting note:
Twice on fresh installs I ran into the following error -

![image](https://user-images.githubusercontent.com/16612216/148631462-ea48c798-f4e5-46a9-8292-4ba67fa596a1.png)

If this happens, move into the project directory ('vehicle' in the example above) and run the following command:

`dotnet add vehicle.csproj package Swashbuckle.AspNetCore -v 6.2.3 -s https://api.nuget.org/v3/index.json`

![image](https://user-images.githubusercontent.com/16612216/148631609-ef8bee80-128c-43ab-88be-8f792f9d7498.png)

Run `code -r ..\vehicle` to reload VS Code with your project (if you didn't have the error above, simply run `code -r vehicle`o

If you get this message, click 'yes':

![image](https://user-images.githubusercontent.com/16612216/148631675-0f45b282-eb93-4d8d-b329-d45af49ce203.png)

Now open the `Program.cs` file in your project.  Lines 17 through 38 should look like this:

![image](https://user-images.githubusercontent.com/16612216/148631711-12669201-d441-49f4-94ef-ed18cdc90d67.png)

Delete everything from lines 19 to 36 and add one line: `app.MapGet("/", () => "Vehicle API");`

![image](https://user-images.githubusercontent.com/16612216/148631761-41522d5a-067c-4418-b69d-dea9cb250b63.png)

From here, save your file and press CTRL+F5 to run a test.  A browser will open and you should have your API running:

![image](https://user-images.githubusercontent.com/16612216/148631813-af17b5ff-a9a1-4dc7-8c7b-14460be68477.png)

In the code, let's add a couple additional GET calls, as well as removing everything after the `app.Run()` line:

![image](https://user-images.githubusercontent.com/16612216/148631882-803e9c4e-608e-4a0b-a68d-bbc4b6ef89ac.png)

After running it again, you should be able to test the three new GET calls.  This is just one sample using `/startengine`

![image](https://user-images.githubusercontent.com/16612216/148631929-117551c1-fd00-45e8-a14e-918a3fdba4bd.png)
