# Use an Adafruit Circuit Playground to make a LED light blink in the SOS distress pattern
In our first Arduino lab you will write a program that will blink an LED light repeatedly in the [SOS distress signal](https://en.wikipedia.org/wiki/SOS) of three short blinks, three long blinks, three more short blinks and then a pause.  The SOS distress signal is used to indicate an emergency and that someone needs help.    
![](SOSblink.gif)  

### Step 1: Plug in the Adafruit Circuit Playground and start the Arduino program
Contact the Circuit Playground to your computer with a USB cord. Then start the Arduino program on your computer. You can find the Arduino program by clicking on the Start Menu at the bottom left of the screen and choosing *Arduino IDE*. Then go to the *Tools* menu and choose *Board | Adafruit Circuit Playground*.  

### Step 2: Run this sample program
Copy and paste the following program
```java {.line-numbers}
#include <Adafruit_CircuitPlayground.h>

// the setup function runs once when you press reset or power the board
void setup() {
  CircuitPlayground.begin();                        // initialize the Circuit Playground  
  CircuitPlayground.setPixelColor(0, 255, 0, 0);    // turn pixel 0 on by making a red color (RGB 255,0,0)
  delay(5000);                                      // wait for 5 seconds (5000 milliseconds)
  CircuitPlayground.clearPixels();                  // turn off all pixels
  delay(5000);                                      // wait for 5 seconds (5000 milliseconds)
}

// the loop function runs over and over again forever
void loop() {

}
```
Click on the *Upload* button to transfer the program to the Arduino and start running. You should see led #13 (just to the right of the USB port labeled `#13`) pulse rapidly as the program is transferred. For 5 seconds, pixel 0 (just to the left of the USB port) should turn on and then it should turn off. Save and name the program something like *BlinkSOS* by choosing *File | Save*.

### Step 3: Modify the sample program to loop repeatedly
Move the last four lines from `setup()` to `loop()`. The program should look like the one below
```java {.line-numbers}
#include <Adafruit_CircuitPlayground.h>

// the setup function runs once when you press reset or power the board
void setup() {
  CircuitPlayground.begin();                        // initialize the Circuit Playground                                  
}

// the loop function runs over and over again forever
void loop() {
  CircuitPlayground.setPixelColor(0, 255, 0, 0);    // turn pixel 0 on by making a red color (RGB 255,0,0)
  delay(5000);                                      // wait for 5 seconds (5000 milliseconds)
  CircuitPlayground.clearPixels();                  // turn off all pixels
  delay(5000);                                      // wait for 5 seconds (5000 milliseconds)
}
```
Click on the *Upload* button to transfer the program to the Arduino and start running. Now you should see pixel 0 blink on and off repeatedly every 5 seconds.  

### Step 4: Write your own program
Using the sample program as a starting point, write your own program to blink the LED in the SOS pattern.  Your finished program should have three functions:
- `void setup()` sets the `pinMode` of led #13
- `void blink(int t)` blinks the LED once for `t` milliseconds
- `void loop()` calls `blinik` and `delay` to create a repeating SOS pattern

### Step 5: Submit the finished program
Submit your finished program by uploading the `BlinkSOS.ino` file to Google classroom. You should be able to find it in *My Documents | Arduino*. Don't forget to click the *Mark as done* button.

### Extensions:
If you have extra time, feel free to experiment. See if you can turn the other pixels to different colors. Look at the sample programs under *File | Examples | Adafruit Circuit Playground, | HelloCircuitPlayground*. Make different patterns, have fun and be creative!
