# LCD_Display_ElegooMega2560
Arduino project integrating a 16x2 or 20x4 LCD display with the Elegoo Mega 2560. Supports both I2C and parallel wiring methods
#include <LiquidCrystal.h> // Include the LiquidCrystal library

Hardware Requirements

Required Components
	•	Elegoo Mega 2560
	•	16x2 or 20x4 LCD Display
	•	I2C Module (PCF8574) (Optional)
	•	10KΩ Potentiometer (For contrast adjustment in parallel wiring)
	•	Jumper wires
	•	Breadboard (Optional for prototyping)
 
// Define the LCD pin numbers
const int rs = 12, en = 11, d4 = 5, d5 = 4, d6 = 3, d7 = 2;

// Initialize the LCD
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);

void setup() {
  // Start the LCD with 16 columns and 2 rows
  lcd.begin(16, 2); 

  // Print "Hello, World!" to the first line
  lcd.print("Hello, World!");
  
  // Move the cursor to the second line
  lcd.setCursor(0, 1);
  
  // Print "Arduino" to the second line
  lcd.print("Arduino");
}

void loop() {
  // Nothing needs to be done in the loop for now
}
