# Use an Arduino to make a LED light blink in the SOS distress pattern
In our first Arduino lab you will write a program that will blink an LED light repeatedly in the [SOS distress signal](https://en.wikipedia.org/wiki/SOS) of three short blinks, three long blinks, three more short blinks and then a pause.  The SOS distress signal is used to indicate an emergency and that someone needs help.    
![](SOSblink.gif)  

### Step 1: Plug in the Arduino and start the Arduino program
You can find the Arduino program by clicking on the Start Menu at the bottom left of the screen and choosing *Arduino IDE*. Then go to the *Tools* menu and choose *Board | Adafruit Circuit Playground*.  

### Step 2: Run this sample program
Copy and paste the following program
```java {.line-numbers}
// the setup function runs once when you press reset or power the board
void setup() { 
  pinMode(13, OUTPUT);      // initialize digital pin 13 as an output.
  digitalWrite(13, HIGH);   // turn the pin 13 LED on (HIGH is the voltage level)
  delay(1000);              // wait for a second (1000 milliseconds
  digitalWrite(13, LOW);    // turn the pin 13 LED off by making the voltage LOW
  delay(1000);           
}

// the loop function runs over and over again forever
void loop() {

}
```
Click on the *Upload* button to transfer the program to the Arduino and start running. You should see led #13 (just to the right of where the USB cord connects) pulse rapidly as the program is transferred and then blink off. Save your program with a name like *BlinkSOS* by choosing *File | Save*.

### Step 3: Modify the sample program to loop repeatedly
Move the last four lines from `setup()` to `loop()`. The program should look like the one below
```java {.line-numbers}
// the setup function runs once when you press reset or power the board
void setup() { 
  pinMode(13, OUTPUT);      // initialize digital pin 13 as an output.       
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(13, HIGH);   // turn the pin 13 LED on (HIGH is the voltage level)
  delay(1000);              // wait for a second (1000 milliseconds
  digitalWrite(13, LOW);    // turn the pin 13 LED off by making the voltage LOW
  delay(1000);    
}
```
Click on the *Upload* button to transfer the program to the Arduino and start running. Now you should see led #13 blink on and off repeatedly.  

### Step 4: Write your own program
Using the sample program as a starting point, write your own program to blink the LED in the SOS pattern.  Your finished program should have three functions:
- `void setup()` sets the `pinMode` of led #13
- `void blink(int t)` blinks the LED once for `t` milliseconds
- `void loop()` calls `blinik` and `delay` to create a repeating SOS pattern

### Step 5: Submit the finished program
Submit your finished program by uploading the `BlinkSOS.ino` file to Google classroom. You should be able to find it in *My Documents | Arduino*. Don't forget to click the *Mark as done* button.
