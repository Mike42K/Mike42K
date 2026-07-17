## Hi there 👋

<!--
**Mike42K/Mike42K** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...



// Declare metavliti as a float and set a starting default value
float metavliti = 100.0; 
const int trigPin = 9;
const int echoPin = 10;

void setup() {
  Serial.begin(9600);
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
}

void loop() {
  // Clear the trigPin by setting it LOW
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  
  // Trigger the sensor with a 10 microsecond HIGH pulse
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
  
  // Read the echoPin, returns the sound wave travel time in microseconds
  long duration = pulseIn(echoPin, HIGH);
  
  // Calculate distance in centimeters
  float distanceCm = duration * 0.0343 / 2;
  
  // Print the prefix
  Serial.print("Distance: ");
  
  if (distanceCm < 300.0 && distanceCm > 0) {
    // If the reading is valid, print it, add "cm", and save it
    Serial.print(distanceCm);
    Serial.println(" cm");
    metavliti = distanceCm;
  } 
  else {
    // If it bugs out, print the last valid distance instead
    Serial.print(metavliti);
    Serial.println(" cm (Fallback)");
  }
  
  delay(500);
}
-->
