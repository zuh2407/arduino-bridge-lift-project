// Motor driver pins
const int IN1 = 8;
const int IN2 = 9;
const int ENA = 10; // PWM pin for motor speed control

void setup() {
  // Set motor pins as output
  pinMode(IN1, OUTPUT);
  pinMode(IN2, OUTPUT);
  pinMode(ENA, OUTPUT);

  // Motor off at start
  digitalWrite(IN1, LOW);
  digitalWrite(IN2, LOW);
  analogWrite(ENA, 0); 
}

void loop() {
  // Clockwise rotation - Lift the bridge
  digitalWrite(IN1, HIGH);
  digitalWrite(IN2, LOW);
  analogWrite(ENA, 200); // Speed (0-255)
  delay(3000); // Motor runs for 3 seconds

  // Stop the motor
  analogWrite(ENA, 0);
  delay(1000); // Wait for 1 second

  // Anticlockwise rotation - Lower the bridge
  digitalWrite(IN1, LOW);
  digitalWrite(IN2, HIGH);
  analogWrite(ENA, 200); // Same speed
  delay(3000); // Motor runs for 3 seconds

  // Stop the motor again
  analogWrite(ENA, 0);
  delay(1000); // Wait before repeating
}
