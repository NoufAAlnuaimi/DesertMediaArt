# DesertMediaArt

### Exercise 1
#### Rainbow: LED Light Color Transition Project Code
 ```
"""Internal RGB LED project"""
import time
import board
print ('Hello World')
if hasattr(board, "APA102_SCK"):
    import adafruit_dotstar
    led = adafruit_dotstar.DotStar(board.APA102_SCK, board.APA102_MOSI, 1)
else:
    import neopixel
    led = neopixel.NeoPixel(board.NEOPIXEL, 1)
    led.brightness = 0.3
while True:
    
#Purple shades
    led[0] = (138,43,226)
    time.sleep(0.5)
    
    led[0] = (148,0,211)
    time.sleep(0.5)
    
    led[0] = (139, 0, 139)
    time.sleep(0.5)
    
    led[0] = (128, 0, 128)
    time.sleep(0.5)
    
    led[0] = (75,0,130)
    time.sleep(0.5)
    
#Blue shades
    led[0] = (0,0,139)
    time.sleep(0.5) 
    
    led[0] = (0,0,205)
    time.sleep(0.5) 
    
    led[0] = (0,0,255)
    time.sleep(0.5)
    
    led[0] = (137, 207, 240)
    time.sleep(0.5)
    
    led[0] = (8, 143, 143)
    time.sleep(0.5)
    
#Green shades
    led[0] = (0, 163, 108)
    time.sleep(0.5)  
    
    led[0] = (0, 128, 0)
    time.sleep(0.5)
 
    led[0] = (34, 139, 34)
    time.sleep(0.5)  
    
   led[0] = (147, 197, 114)
    time.sleep(0.5)        
    
    led[0] = (217, 217, 33)
    time.sleep(0.5)
    
#Yellow shades
   led[0] = (255, 234, 0)
    time.sleep(0.5)
    
   led[0] = (225, 193, 110)
    time.sleep(0.5)
    
    led[0] = (255, 247, 0)
    time.sleep(0.5)
    
    led[0] = (253, 218, 13)
    time.sleep(0.5)
    
    led[0] = (255, 215, 0)
    time.sleep(0.5)
    
#Orange Shades
    led[0] = (244, 187, 68)
    time.sleep(0.5)
    
    led[0] = (255, 170, 51)
    time.sleep(0.5)
    
    led[0] = (228, 155, 15)
    time.sleep(0.5)
    
    led[0] = (255, 165, 0)
    time.sleep(0.5)
    
    led[0] = (255, 87, 51)
    time.sleep(0.5)
    
#Red Shades
   led[0] = (255, 69, 0)
    time.sleep(0.5)

    led[0] = (255, 0, 0)
    time.sleep(0.5)
    
    led[0] = (178,34,34)
    time.sleep(0.5)
    
    led[0] = (139,0,0)
    time.sleep(0.5)
    
    led[0] = (128,0,0)
    time.sleep(0.5)
  ```


### Exercise 3
#### Light Friend
 ```
import time
import board
import analogio
import digitalio
import neopixel

# Set the pin for the LDR (Light-Dependent Resistor)
ldr_pin = analogio.AnalogIn(board.A1)
ldr_pin2 = analogio.AnalogIn(board.A3)

# Set the pin for the NeoPixel ring
pixel_pin = board.D5
num_pixels = 12

# Create NeoPixel object
pixels = neopixel.NeoPixel(pixel_pin, num_pixels, brightness=0.2)

# Define the LDR threshold
#darkness
threshold = 3000
threshold2 = 3000

# for bright light
threshold3 = 30000
threshold4 = 30000


print("Enabling NeoPixel power!")
enable = digitalio.DigitalInOut(board.D10)
enable.direction = digitalio.Direction.OUTPUT
enable.value = True   
   
while True:
    ldr_value = ldr_pin.value
    ldr_value2 = ldr_pin2.value
    print("LDR Value:", ldr_value)
    print("LDR Value2:", ldr_value2)

    if ldr_value < threshold:
        pixels[0] = (0, 0, 255)
        pixels[1] = (0, 0, 255)
        pixels[2] = (0, 0, 255)
        pixels[3] = (0, 0, 255)
        pixels[4] = (0, 0, 255)
        pixels[5] = (0, 0, 255)
 
    else:
       pixels.fill((255, 255, 255))
        
    if ldr_value2 < threshold2:
    
        pixels[6] = (0, 255, 255)
        pixels[7] = (0, 255, 255)
        pixels[8] = (0, 255, 255)
        pixels[9] = (0, 255, 255)
        pixels[10] = (0, 255, 255)
        pixels[11] = (0, 255, 255)

#when brightness is high

    if ldr_value > threshold3:
    
        pixels[6] = (0, 255, 0)
        pixels[7] = (0, 255, 0)
        pixels[8] = (0, 255, 0)
        pixels[9] = (0, 255, 0)
        pixels[10] = (0, 255, 0)
        pixels[11] = (0, 255, 0)

    if ldr_value2 > threshold4:
        pixels[0] = (255, 255, 0)
        pixels[1] = (255, 255, 0)
        pixels[2] = (255, 255, 0)
        pixels[3] = (255, 255, 0)
        pixels[4] = (255, 255, 0)
        pixels[5] = (255, 255, 0)

        
    pixels.show()
    time.sleep(0.25)  #delay for visibility and LDR reading

   ```

![IMG_9137](https://github.com/NoufAAlnuaimi/DesertMediaArt/assets/144128799/a0da5d22-f1bf-4c96-aa08-140e3483169f)
![IMG_9136](https://github.com/NoufAAlnuaimi/DesertMediaArt/assets/144128799/422c77c9-e2cd-426c-98d4-2318cf0ecfb9)
![IMG_9098](https://github.com/NoufAAlnuaimi/DesertMediaArt/assets/144128799/d33d2af7-082f-4579-8610-d957a25588ac)


[Video Demo] (https://drive.google.com/file/d/1F8iX1j2sUEi0TorR-WuuP_OVvw26NUPI/view?usp=sharing).


#### Circuit Diagram
![circuirdiagram](https://github.com/NoufAAlnuaimi/DesertMediaArt/assets/144128799/10bdb9fe-0ff9-49c7-88b9-d32e9d75f567)



