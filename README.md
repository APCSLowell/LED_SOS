# Use an Arduino to make a LED light blink in the SOS distress pattern
In our first Arduino lab you will write a program that will blink an LED light repeatedly in the [SOS distress signal](https://en.wikipedia.org/wiki/SOS) of three short blinks, three long blinks, three more short blinks and then a pause.  The SOS distress signal is used to indicate an emergency and that someone needs help.    
![](SOSblink.gif)  

### Step 1: Plug in the Arduino and start the Arduino program
You can find the Arduino program by clicking on the Start Menu at the bottom left of the screen and choosing *Arduino IDE*. Then go to the *File* menu and open the program *Examples | 01 Basics | Blink*. Now go to the *Tools* menu choose *Board | Adafruit Circuit Playground*.  Click on the *Upload* button to transfer the program to the Arduino and start running. You should see led #13 (just to the right of where the USB cord connects) blink on and off.

  
### Step 2: Write your own program
Start a new program by choosing *File | New*. Using the Blink program as an example, write your own program to blink the LED in the SOS pattern. Save your program with a name like *BlinkSOS*. Your finished program should have four functions:
- `void setup()` sets the `pinMode` of led #13
- `void blink(int time)` blinks the LED once for a `time` milliseconds
- `void loop()` calls `blinik` and `delay` to create a repeating SOS pattern

### Step 3: Submit the finished program
Submit your finished program by uploading the `BlinkSOS.ino` file to Google classroom. You should be able to find it in *My Documents | Arduino*. Don't forget to click the *Mark as done* button.
