# Create your custom image classifier for Watson Visual Recognition service

This extension enables you to create your own custom image classifiers 

<p align="center">
  <img src="wvr.png"/ width=300px>
</p>

service demo:
https://visual-recognition-demo.mybluemix.net/train

# Before you start

1. Sign up an IBM Bluemix acount.

	https://console.ng.bluemix.net/registration/?target=%2Fdashboard%2Fapps
	
	or log in to an existing one
	
2. Create new app
	1. In your dashboard click on 'Create App'
	2. Find 'Visual Recognition'
	3. Fill out the form and proceed with 'Create' button
	
3. Aquire service 'api_key'
	1. On your service's main page click 'Service Credentials' tab.
	2. From the list choose your credentials and click on 'View Credentials'
	3. Copy Your 'api_key'.
	

4. SPSS Modeler and R requirements:
	- SPSS Modeler v18.0
	- SPSS Modeler 'R essentials' plugin
	- R packages: 
		- httr
		- RJSONIO
		- RCurl
		
5. Install WatsonCreateClassifier extension from SPSS Modeler Extension Hub.


# Example usage
## Creating classifier

Example stream

<p align="center">
  <img src="Screenshot/stream.PNG"/ width=300px>
</p>


WatsonCreateClassifier node requires a connected source with your 'api_key' for bluemix services. 

<p align="center">
  <img src="Screenshot/input1.PNG"/ width=300px>
</p>

	
In the main node window coose your 'api_key' in the 'Watson Api Key' field. Next provide 'Name', 'Class Name' and choose files that contain examples representing your 'Class Name' and some examples representing their opposites.

<p align="center">
  <img src="Screenshot/input2.PNG"/ width=300px>
</p>
	
	
# Output

The generated output is a table that contains the the classifier name, it's id assigned by the Watson, name of the positive class examples and path to files that were used for training.
If you wish to use your new classifier in other nodes save the 'classifier ID'!



<p align="center">
  <img src="Screenshot/output.PNG"/ width=500px>
</p>

You can test how well your classifier works using the ['WatsonVisualRecognition'][2] extension!



# License
- [Apache 2.0][1]

# Contributors
- Artur Kucia

 [1]: http://www.apache.org/licenses/LICENSE-2.0.html
 [2]: https://github.com/SpssModelerExtensions/WatsonVisualRecognition
