# Anodophyton
Array em python, para um display de sete seguimentos no Wokwi




# Link do Wokwi: <br>
https://wokwi.com/projects/373877550709754881

 <h4> Código: </h4>
 
import utime <br>
from machine import Pin <br>

leds = [1,2,3,4,5,6,7,8] <br>

nums = [ <br>
    [1,0,0,1,1,1,1,1], <br>
    [0,0,1,0,0,1,0,1], <br>
    [0,0,0,0,1,1,0,1], <br>
    [1,0,0,1,1,0,0,1], <br>
    [0,1,0,0,1,0,0,1], <br>
    [0,1,0,0,0,0,0,1], <br>
    [0,0,0,1,1,1,1,1], <br>
    [0,0,0,0,0,0,0,1], <br>
    [0,0,0,0,1,0,0,1], <br>
    [0,0,0,0,1,0,0,0], <br>
  ] <br>
for index in range(8): <br>
  leds[index] = Pin(leds[index],Pin.OUT) <br>

def ligar(oqueFazer): <br>
  for index in range(8): <br>
    leds[index].value(oqueFazer[index]) <br>

while True: <br>
  for index in range(10): <br>
    ligar(nums[index]) <br>
    utime.sleep(0.7) <br>



