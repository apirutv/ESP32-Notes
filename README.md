# ESP32-Notes

### ESP32 and Arduino IDE

https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-windows-instructions/

### ESP32 and Mycropython

https://randomnerdtutorials.com/flashing-micropython-firmware-esptool-py-esp32-esp8266/


### REPL, rshell

https://www.youtube.com/watch?v=5W3WvXAmDJc

https://github.com/dhylands/rshell


### OLED

https://www.instructables.com/id/MicroPython-on-an-ESP32-Board-With-Integrated-SSD1/

Wiring Diagram

https://www.arduinoall.com/product/3062/esp32-oled-v2-esp32-oled-wifi-module-bluetooth-บอร์ด-esp32-พร้อมจอ-oled

## MUST WRITE 1 TO RESET PIN FIRST

oterwise will recieve OSError: [Errno 19] ENODEV

  import machine, ssd1306_AV<br/>
  from machine import Pin<br/>
  rst=Pin(16,Pin.OUT)<br/>
  rst.value(1)<br/>
  i2c = machine.I2C(scl=machine.Pin(15), sda=machine.Pin(4))<br/>
  oled = ssd1306_AV.SSD1306_I2C(128, 64, i2c)<br/>
  oled.fill(0)<br/>
  oled.text('hello world',0,0)<br/>
  oled.show()<br/>

see source git
