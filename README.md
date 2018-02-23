# Things-Connected-Create-an-Application
Creating a Sigfox application on the things connected portal

1. Select Sigfox to make sure we are creating a sigfox application
2. Select Applications on the left hand menu

![Screenshot](screenshots/tca001.png)


1. Select create new on the menu on the left hand side this will display the form to create the application
2. Enter a name that you can idenify the application by.
3. Enter the URL of where the messages need to be sent
4. The callback subtype should be set to BIDIR so we can use two way messaging.
5. The HTTP method your server expects to recieve the messages by. As we are usually writing data this should be POST.
6. The formatting of the 12 bytes being recieved in this case we are converting the bytes into a decimal so 0-255.
```
{{device}#{seqNumber}#{station}#{rssi}#{customData#int1}#{customData#int2}#{customData#int3}#{customData#int4}#{customData#int5}#{customData#int6}#{customData#int7}#{customData#int8}#{customData#int9}#{customData#int10}#{customData#int11}#{customData#int12}}
```
7. This formats the fields to be posted to your applicatin server.
```
{ 					
	"temperature" : "{customData#int1}.{customData#int2}", 
	"humidity" : "{customData#int3}.{customData#int4}" ,
	"temperature1" : "{customData#int5}.{customData#int6}", 
	"humidity1" : "{customData#int7}.{customData#int8}" , 
	"temperature2" : "{customData#int9}.{customData#int10}", 
	"humidity2" : "{customData#int11}.{customData#int12}" , 
	"device" : "{device}", 
	"deviceType" : "Bluefox", 
	"time" : "{time}", 
	"station" : "{station}", 
	"rssi" : "{rssi}", 
	"seqNumber" : "{seqNumber}" 
}
```

8. As we are sending JSON Formatted data we set this to application/json
9. Click next to complete the application setup

![Screenshot](screenshots/tca002.png)


1. We now need to connect devices to our application. Select devices from the left hand menu

c

1. On the right hand side select the icon for the drop down box
2. Select your application from this list, in my case it was 'My First Application'


![Screenshot](screenshots/tca004.png)

The box on the right hand side should now display your application connected to the chosen device.

![Screenshot](screenshots/tca005.png)
