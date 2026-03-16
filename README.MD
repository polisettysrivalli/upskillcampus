// Smart Home Automation using Arduino and Bluetooth

char data;              // variable to store data
int light = 7;          // light connected to pin 7
int fan = 8;            // fan connected to pin 8

void setup()
{
  Serial.begin(9600);

  pinMode(light, OUTPUT);
  pinMode(fan, OUTPUT);

  digitalWrite(light, LOW);
  digitalWrite(fan, LOW);
}

void loop()
{
  if (Serial.available() > 0)
  {
    data = Serial.read();
  }

  // Light Control
  if (data == 'A')
  {
    digitalWrite(light, HIGH);
  }

  if (data == 'a')
  {
    digitalWrite(light, LOW);
  }

  // Fan Control
  if (data == 'B')
  {
    digitalWrite(fan, HIGH);
  }

  if (data == 'b')
  {
    digitalWrite(fan, LOW);
  }
}
