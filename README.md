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

}```

### Evidence
[Here is my link to arduino] (https://create.arduino.cc/editor/lkuhlma22/163be499-bd49-4efe-bfe1-71275229e557)

### Image or Wiring

### Reflection
It was pretty easy once I understood the conditions.  A condition is basically just an if then statement.
