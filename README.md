# MyCalculatorAzure-Function-App-calculator
Using Http Trigger to call an Azure-Function-App that sums the value of x and y and inputs a result

The app is tested locally and later published to Azure and also tested in Azure using http as it's trigger.

The class was renamed to sum

The function attribute was also renamed to sum

The content of run method was deleted

The logger was not deleted

Lines as shown below were added

int x =int.Parse(req.Query["x"]);

int y =int.Parse(req.Query["y"]);

int result = x + y;

return new OkobjectResult(result);

The parseInt method parses a value as a string and returns the first integer

the sum was calculated in the local environment using the link that was thrown to the debugger http://localhost:7071/api/sum?x=4&y=6

The sum was calculated in Azure platform using the link that was gotten from get function url in the function tab of azure function app that was created earlier

https://mycalculatorap.azurewebsites.net/api/Sum?code=TLE4CaQIVAib7Qt18lO1tJTKEdsvuQgMS5X8DE_aeDtlAzFu4MBocg==&x=50&y=56
