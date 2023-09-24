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
    
