# Lyrics-Box-Arduino
It's just a prototype I am working on to display Lyrics based on time.
In this demo, I have used the song Closer from Chainsmokers. 

Requirements

Arduino
Breadboard
16X2 LCD Display
Jumpwires
PC with Arduino

Setup 

Download the file and open it with Arduino. 
Upload the file to your board. 
Using the serial monitor, Send "N" to start displaying the lyrics.

Source Code :
```
#include <LiquidCrystal.h>
char ch;
int Contrast=15;
// initialize the library with the numbers of the interface pins
LiquidCrystal lcd(12, 11, 5, 4, 3, 2);

void setup() 
{
  Serial.begin(9600);
  Serial.println("LCD test with PWM contrast adjustment");
  
  analogWrite(6,Contrast);
  // set up the LCD's number of columns and rows: 
  lcd.begin(16, 2);
  // Print a message to the LCD.
  lcd.print("Closer");
  lcd.setCursor(0,1);
  lcd.print("The Chainsmokers");
}
void loop()
{
  analogWrite(9,28836);
}
  
void serialEvent()
{
     if (Serial.available())
  {
 ch= Serial.read();
     if(ch=='N')
     {

      lcd.setCursor(0,0);
      lcd.print("So Baby Pull Me     ");
      lcd.setCursor(0,1);
      lcd.print("Closer               ");
      delay(2000);
 lcd.setCursor(0,0);
      lcd.print("In The Backseat");
      lcd.setCursor(0,1);
      lcd.print("of your Rover       ");
      delay(2910);
       lcd.setCursor(0,0);
      lcd.print("That I know you    ");
      lcd.setCursor(0,1);
      lcd.print("can't Afford       ");
      delay(2300);
       lcd.setCursor(0,0);
      lcd.print("Bite that Tattoo    ");
      lcd.setCursor(0,1);
      lcd.print("on your shoulder     ");
      delay(2660);
       lcd.setCursor(0,0);
      lcd.print("Pull the Sheets      ");
      lcd.setCursor(0,1);
      lcd.print("Right off the        ");
      delay(1500);
       lcd.setCursor(0,0);
      lcd.print("Right off the         ");
      lcd.setCursor(0,1);
      lcd.print("Corner               ");
      delay(860);
       lcd.setCursor(0,0);
      lcd.print("Of the Mattress   ");
      lcd.setCursor(0,1);
      lcd.print("that you Stole   ");
      delay(2360);
       lcd.setCursor(0,0);
      lcd.print("From ur Roommate");
      lcd.setCursor(0,1);
      lcd.print("back in Boulder ");
      delay(2670);
       lcd.setCursor(0,0);
      lcd.print("We ain't ever     ");
      lcd.setCursor(0,1);
      lcd.print("getting Older     ");
      delay(2715);
       lcd.setCursor(0,0);
      lcd.print("                  ");
      lcd.setCursor(0,1);
      lcd.print("                  ");
      delay(7556);
       lcd.setCursor(0,0);
      lcd.print("We ain't ever     ");
      lcd.setCursor(0,1);
      lcd.print("getting Older     ");
      delay(2830);
       lcd.setCursor(0,0);
      lcd.print("                    ");
      lcd.setCursor(0,1);
      lcd.print("                    ");
      delay(7450);
        lcd.setCursor(0,0);
      lcd.print("We ain't ever     ");
      lcd.setCursor(0,1);
      lcd.print("getting Older     ");
      delay(300000);
      
     }
  }
}
```
