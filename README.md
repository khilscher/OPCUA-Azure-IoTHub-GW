# OPCUA-Azure-IoTHub-GW
OPC UA to Azure IoT Hub Gateway

Code is based on the OPC Foundation OPC UA .Net Standard Library Stack at https://github.com/OPCFoundation/UA-.NETStandardLibrary

## Build Steps
- Clone this repo
- Open the solution using Visual Studio 2017
- Set the startup project to **NetCoreConsoleClient**
- Update ```Program.cs``` in the NetCoreConsoleClient project as follows
  - Line 30 - update this to the device name you registered in IoT Hub
  - Line 35 - update this with the connection string of the device you registered in IoT Hub. You can obtain this using the Azure Portal or Device Explorer.
  - Line 44 - update the endpointURL with the URL of your OPC UA server or pass this value in as a parameter.
  - Line 65 - change IoT Hub transport protocol from ```TransportType.Amqp``` to ```TransportType.Http``` or ```TransportType.Mqtt``` if desired. Recommend using MQTT or AMQP.
  - Line 200 to 208 - update with tags you wish to subscribe to coming from your OPC UA server. For formatting of NodeIDs, refer to http://documentation.unified-automation.com/uasdkhp/1.0.0/html/_l2_ua_node_ids.html
- Build and run  
