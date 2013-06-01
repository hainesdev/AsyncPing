#AsyncPing Library

This library allows your arduino sketches to take ultrasonic distance readings at a fast rate. Your application can
call the AsyncPing function repeatedly to get distance readings. No timing to worry about. While the arduino
is waiting for an echo no additional pulses are sent. Time in between pulse and echo can be used for other functions.

This code is based on the NewPing library. I have crafted this code in an attempt optimize and remove the delay()'s from NewPing.

###Synopsis

AsyncPing Ping;
void setup()
{
  Serial.begin(115200);  
 }
void loop()
{
   Serial.println(Ping.distance(900));
}

##Library Reference

``unsigned long Ping.distance(int Accuracy)``

'Accuracy' - the amount of time devoted to the ultra sonic reading. This value is dependent on how often the function is called.


##Installation

Move the Folder ``AsyncPing`` directory to
``~/arduino/libraries/AsyncPing/`` and restart your Arduino IDE.
Try out the examples!


##Notes
This code was made with sample rate and stability in mind. Taking readings in any established unit (in, cm) has not been tried.