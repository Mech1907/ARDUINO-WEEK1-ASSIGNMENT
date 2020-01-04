// constants won't change. They're used here to set pin numbers:
const int buttonPin1 = 23;     // the number of the pushbutton pin
const int buttonPin2 = 24;
const int ledPin1 =  2;      // the number of the LED pin

// variables will change:
int buttonState1 = 0;         // variable for reading the pushbutton status
int buttonState2 = 0;

void setup() {
  pinMode(ledPin1, OUTPUT);
  pinMode(buttonPin1, INPUT);
  pinMode(buttonPin2, INPUT);
}

void loop() {
  buttonState1 = digitalRead(buttonPin1);
  buttonState2 = digitalRead(buttonPin2);

  if ((buttonState1 == HIGH) && (buttonState2 == LOW)) {
    digitalWrite(ledPin1, HIGH);
  }
  if ((buttonState1 == LOW) && (buttonState2 == HIGH)) {
    digitalWrite(ledPin1, HIGH);
  }
  else {
    digitalWrite(ledPin1, LOW);
  }
}
