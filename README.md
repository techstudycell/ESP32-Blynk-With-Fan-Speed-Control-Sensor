# ESP32-Blynk-With-Fan-Speed-Control-Sensor
In this IoT project, I have shown how to make IoT-based Smart Home Automation using ESP32 Google Assistant Blynk with the timer, sensor, and IR remote control relay with real-time feedback.

So, you can easily make this home automation project at home just by using an ESP32 and relay module. Or you can also use a custom-designed PCB for this project.

## Tutorial Video on IoT Project using ESP32 & Blynk
https://youtu.be/vBq3Ozrwj-4

## This Blynk ESP32 control smart relay has the following features:

1. Control home appliances with WiFi (Blynk IoT App).
2. Control ceiling fan speed with Blynk, IR Remote, & selector switch.
3. Control home appliances with an IR remote.
4. Control home appliances with manual switches or push buttons.
5. Save thelast GPIO state in ESP32 flash memory.
6. Monitor real-time room temperature in the Blynk IoT App
7. Monitor real-time feedback in the Blynk IoT App.
8. Control appliances, and fan speed without WiFi.

## Required components for the ESP32 Project
So, you can easily make this home automation project at home just by using an ESP32 and relay module. Or you can also use a custom-designed PCB for this project.
Required components:
1. ESP32 DevKIT V1
2. 4-channel 5V SPDT Relay Module
3. DHT11 Sensor
4. TSOP1838 IR Receiver (with metallic case)
5. Switches or Pushbuttons
6. Any IR Remote
7. 4-step Fan Regulator OR (2.2uf & 3.3uf 250V Capacitor, 2.2-ohm 1/2W Resistors, 220k 1/4W Resistors, and 4-step selector switch)

## Circuit Diagram of the ESP32 IoT Project
The circuit is very simple, I have used the GPIO pins D23, D22, D21 & D19 to control the 4 relays.
And the GPIO pins D13, D12, D14 & D27 are connected with switches, and GPIO D33, D32, D15 & D4 are connected with a 4-step selector switch to control the 4 relays manually.
I used the INPUT_PULLUP function in Arduino IDE instead of the pull-up resistors.
IR remote receiver (TSOP1838) connected with D35. And the DHT11 sensor is connected to RX2 (GPIO-16).
I have used a 5V mobile charger to supply the smart relay module.

Please take proper safety precautions while working with high voltage.

## Control Fan Speed With Blynk IoT App
Control the speed of the ceiling fan from anywhere in the world from the Blynk IoT App. If the WiFi is connected, you can also monitor the real-time feedback in the Blynk.

## Control Fan Speed With IR Remote and Selector Switch
You can use any IR remote to control the fan speed. I have used 2 buttons to increase and decrease the fan speed from the IR remote.
You can also use a selector switch to control the fan speed manually if the WiFi is not connected.

## Control Relays With Blynk, IR Remote and Manual Switch
If the ESP32 is connected to WiFi, you can control the home appliances from Blynk IoT App.

You also use multiple smartphones to control the appliances with Blynk App. For that, you have to log in same Blynk account from all the smartphones.

This way, all smartphones will be in the sink to the Blynk server. You can control, and monitor the real-time status of the relays, room temperature & humidity from anywhere in the world in the Blynk IoT App.

You can always control the relays from the IR remote or switches. For this project, you can use any IR remote.

You can monitor the real-time feedback in the Blynk IoT App if the WiFi is connected.

I have explained how to get the IR codes (HEX codes) from any remote in the following steps.

Please refer to the circuit diagram to connect the switches.

## Design the PCB for This Smart Home System
To make the circuit compact and give it a professional look, I designed the PCB after testing all the features of the smart relay module.

You can download the PCB Gerber, BOM, and "pick and place" files of this ESP32 control relay PCB from the following link:

GitHub link to Download PCB Gerber File

For this project, I have the JLC SMT Service while ordering the PCB.

## Why you should use JLC SMT Service?
On JLCPCB's one-stop online platform, customers enjoy low-cost & high-quality & fast SMT service at an $8.00 setup fee($0.0017 per joint).

$27 New User coupon & $24 SMT coupons every month.
Visit https://jlcpcb.com

JLCPCB SMT Parts Library 200k+ in-stock components (689 Basic components and 200k+ Extended components)

Parts Pre-Order service https://support.jlcpcb.com/article/164-what-is-jlcpcb-parts-pre-order-service

Build a Personal library Inventory, save parts for now or the future

Assembly will support 10M+ parts from Digikey, mouser.

## Steps to Order the PCB Assembly from JLCPCB
1. Visit https://jlcpcb.com/RAB and Sign in / Sign up.
2. Click on the QUOTE NOW button.
3. Click on the "Add your Gerber file" button. Then browse and select the Gerber file you have downloaded.
4. Set the required parameter like Quantity, PCB masking color, etc.
5. Select the Assemble side and SMT Quantity.
6. Now upload the BOM and PickAndPlace files.
7. Now confirm all the components which you want to be soldered by SMT services.
8. Click on SAVE TO CART button.
9. Type the Shipping Address.
10. Select the Shipping Method suitable for you.
11. Submit the order and proceed with the payment.

You can also track your order from the JLCPCB.
My PCBs took 3 days to get manufactured and arrived within a week using the DHL delivery option.
PCBs were well packed and the quality was really good at this affordable price.

## Create Blynk Cloud FREE Account & Blynk Template
For this smart house project, I have used the Blynk IoT Cloud Free plan.

Click on the following link to create a Blynk Cloud account.
https://blynk.cloud/dashboard/register

1. Enter your email ID, then click on "Sign Up".
2. You will receive a verification email.
3. Click on Create Password in the email, Then set the password, and click on Next.
4. Enter your first name, and click on Done.
5. After that Blynk cloud dashboard will open.

Create a New Template in Blynk Cloud

First, you have to create a template in the Blynk cloud.

1. Click on New Template.
2. Enter a template name, select the hardware as ESP32, and the connection type will be WiFi.
3. Then click on DONE.
4. You will get the BLYNK_TEMPLATE_ID and BLYNK_DEVICE_NAME after creating the temple.

## Create a Datastream in Blynk Cloud
After that, you have to create Datastreams. Here I will control 4 relays, so I have to create 4 Datastreams. And for Fan Speed Control 1 Datastream.

Steps to add Datastreams.

1. Go to the Datastreams tab.
2. Click on New Datastream and select Virtual Pin.
3. Enter a name, select the virtual pin V1, and the datatype will be Integer.
4. Then click on Create.

In a similar way, create 4 datastreams with virtual pin V1 to V4. And 1 datastream (V5) to turn off all the relays. And for Fan Speed Control 1 Datastream (V0) with MAX value 4 & MIN value = 0.

And for the Temperature and humidity, I have used V6, & V7 (Please refer to the picture or tutorial video).

## Set Up Blynk Cloud Web Dashboard
Now go to the Web Dashboard tab.

Drag and drop 4 Switch widgets, 1 Slider widget, and 2 Level widgets.

Go to the settings of each widget, and select a Datastream.

Please refer to the tutorial video for more details.

Then click on Save to save the template.

## Add Device Using Template in Blynk IoT
Steps to add a device in the Blynk IoT cloud:

1. First, go to Device, then click on "New Device".
2. Click on "From template".
3. Select the Template, and give the device name.
4. Click on Create.

Then in the device info tab, you will get the Blynk Auth Token, Template ID, and Device Name. All these details will be required in the code.

## Get the IR Codes (HEX Code) From the Remote
Now, to get the HEX codes from the remote, first, we have to connect the IR receiver output pin with GPIO D35.

And give the 5V across the VCC and GND. The IR receiver must have a metallic casing, otherwise, you may face issues.

Then follow the following steps to get the HEX codes

1. Install the IRremote library in Arduino IDE
2. Download the attached code, and upload it to ESP32.
3. Open Serial Monitor with Baud rate 9600.
4. Now, press the IR remote button.
5. The respective HEX code will populate in the serial monitor.
Save all the HEX codes in a text file.

## Program the ESP32 for This Blynk Project
GitHub Link to download the Source Code

Download and install the following libraries in Arduino IDE

1. Blynk Library (1.1.0): https://github.com/blynkkk/blynk-library
2. AceButton Library (1.9.2): https://github.com/bxparks/AceButton
3. IRremote Library (3.6.1): https://github.com/Arduino-IRremote/Arduino-IRremote
4. DHT Library (1.4.3): https://github.com/adafruit/DHT-sensor-library
5. Now open the main sketch (code).
6. In the code, you have to update the BLYNK_TEMPLATE_ID, BLYNK_DEVICE_NAME, Auth Token, WiFi Credentials.
7. Then update the HEX codes of the IR remote as shown in the tutorial video.
8. After that, select the DOIT ESP32 DEVKIT V1 board and proper PORT.
9. Then upload the code to ESP32 Board.

While uploading the code to ESP32, if you use the PCB then you will see the "Connecting....___" text, then press and hold the BOOT button and then press the EN button, after that release both buttons.

## Install Blynk IoT App to Configure Mobile Dashboard
1. Install the Blynk IoT app from Google Play Store or App Store. Then log in.
2. Go to Developer Mode.
3. Tap on the template that you have already made.
4. Now go to the Widget box (on the right) to add widgets.
5. Add 5 Button widgets, 1 Slider, and 2 Gauge widgets from Widget Box.
6. Go to the Button widget settings.
7. Enter the name, select Datastream, Mode will be Switch. Then exit.
8. After setting all the Buttons tap on exit.

## Finally!! the Blynk Smart Home System Is Ready
Now you can control your home appliances in a smart way.

I hope you have liked this new Blynk IoT home automation project. I have shared all the required information for this project.

I will really appreciate it if you share your valuable feedback. Also if you have any queries please write in the comment section.

Thank you & Happy Learning.
