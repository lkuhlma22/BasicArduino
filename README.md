# BasicArduino
I'm going to learn how to use an Arduino, and make awesome things with it!


## TableofContents
* [TableOfContents](#TableOfContents)
* [HelloArduino](#HelloArduino)
* [FiniteLEDBlink](#FiniteLEDBlink)

## HelloArduino

### Description & Code
The goal was to make the LED blink 2 times a second.  I did that by speeding up the delay in between blinks.
```C++
// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(450);                       // wait for 13 seconds
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(450);                       // wait for 13 seconds
}

```

### Evidence
[Here is my code on Arduino Create](https://create.arduino.cc/editor/lkuhlma22/0acb39da-2ba7-4df4-badb-d64f4e7550ab)

### Image or Wiring
<img src="http://troybaverstock.com/wp-content/uploads/2019/04/arduino-servo-button-red-green-RGB-LED-wiring-diagram.png" width="300px" /> 

Image credit belongs to [Troy Baverstock](https://troybaverstock.com/learn/fritzing-circuit-diagrams/)

### Reflection
I was pretty lost at first but it became easier when I started to pay more attention to detail.  It was frustrating because even 1 wrong capitalization and none of it would work.
## FiniteLEDBlink

### Description & Code
The goal was tot make the LED blink 5 times and then stop.  We had to use conditions which was an added step from the Hello Arduino assignment.
```C++
int myAge = 0;

void setup() {
  pinMode(LED_BUILTIN, OUTPUT);
  Serial.begin(9600);
}



void loop() {
  myAge = myAge + 1;
  if (myAge <=5) {
    digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
    delay(400);                       // wait for 13 seconds
    digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
    delay(400);                       // wait for 13 seconds

    Serial.println(myAge);

  }
  delay(1000);

}

```

### Evidence
[Here is my link to arduino](https://create.arduino.cc/editor/lkuhlma22/163be499-bd49-4efe-bfe1-71275229e557)

### Image or Wiring

### Reflection
It was pretty easy once I understood the conditions.  A condition is basically just an if then statement in code language.  Its still hard for me to know where to put certain commands.

### One button one LED

### Description and code
The goal of the assignment is to make the LED start blinking when the button is pressed and turn off when the button is released.  
// Button-based Variable LED Blink
  // When I press the button, the LED will blink, then blink faster and faster.
  // Letting go of the button stops the blinking and resets the blink speed to 1 second

  // the setup function runs once when you press reset or power the board
*/
int LED = 13;
int buttonState = 0;
int buttonPin = 7;
int delayVar = 1000;

void setup() {

  // initialize digital pin 13 as an output.
  pinMode(LED, OUTPUT);
  pinMode(buttonPin, INPUT);

  Serial.begin(9600); // This turns on my Serial Monitor
}

void loop() {
buttonState=digitalRead(buttonPin);

  Serial.print("button State: ");
  Serial.print(buttonState);

  if (buttonState == HIGH) {
    digitalWrite(LED, HIGH);           // turn the LED on (HIGH is the voltage level)
    delay(delayVar);                       // wait for a second
    digitalWrite(LED, LOW);            // turn the LED off by making the voltage LOW
    delay(delayVar);                       // wait for a second
    Serial.print("\t delayVar:");
    Serial.println(delayVar);
  }
  else
  {
    digitalWrite(LED, LOW);            // turn the LED off by making the voltage LOW
    Serial.println("\t no blink!");

  }
}

### Evidence
[Here is my code on Arduino Create](https://create.arduino.cc/editor/lkuhlma22/83988797-7935-4019-b121-39519c29f56f)

### Reflection
This assignment was very difficult to me because I do not really know how to code very well.  I kind of understand the concept but i dont understand all the little rules and how nothing works just because of one capitilization error.  The wiring was also very tricky for me to figure out but with help I did.

### 2 Button Servo

### Description and code
The goal of the assignment is to make a servo go clockwise 90 degrees when one button is pushed and go counter clockwise 90 degrees when another button is pushed.  Unfortunently I did not have enough wires in my kit and I had no transportation to chs to get more so I did it with one button.

/*
  
*/
#include <Servo.h>
int buttonState = 0;
int buttonPin = 7;
int delayVar = 1000;

Servo myServo;

void setup() {

  // initialize digital pin 13 as an output.
  pinMode(buttonPin, INPUT);

  Serial.begin(9600); // This turns on my Serial Monitor

 //initializing my servo on pin 9 
  myServo.attach(9);
  
}

void loop() {
buttonState=digitalRead(buttonPin);
  Serial.print("button State: ");
  Serial.print(buttonState);

  if (buttonState == HIGH) {
    myServo.write(180);
  }
  else
  {
   myServo.write(90);
  }
}

### Evidence
[My code in Arduino](https://create.arduino.cc/editor/lkuhlma22/d7d652f1-dd47-442d-bcd8-caf9c6bf5d56)

### Reflection
This one was also very difficult for me because I did not have the right wires and I still dont really understand arduino very well.  It is like trying to learn a new language that has a bunch of rules and if one little thing is wrong none of it makes sense.
