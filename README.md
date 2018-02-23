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
6. The formatting of the data being recieved in this case we are converting the bytes into a decimal so 0-255.
```
{{device}#{seqNumber}#{station}#{rssi}#{customData#int1}#{customData#int2}#{customData#int3}#{customData#int4}#{customData#int5}#{customData#int6}#{customData#int7}#{customData#int8}#{customData#int9}#{customData#int10}#{customData#int11}#{customData#int12}}
```
7.
8.
9.

![Screenshot](screenshots/tca002.png)



