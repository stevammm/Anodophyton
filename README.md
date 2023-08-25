<h1> Anodophyton </h1>
<h4>Array feito em python, para um display de sete seguimentos, demonstrar seus números.</h4>
<br>
<hr>
Link do Wokwi: <br>
https://wokwi.com/projects/373877550709754881
<hr>

 <h3> Código: </h3>
<hr>
 
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



