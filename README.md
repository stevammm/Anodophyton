# Anodophyton
Array em python, para um display de sete seguimentos no Wokwi


//Código:


import utime
from machine import Pin

leds = [1,2,3,4,5,6,7,8]

nums = [
    [1,0,0,1,1,1,1,1],
    [0,0,1,0,0,1,0,1],
    [0,0,0,0,1,1,0,1],
    [1,0,0,1,1,0,0,1],
    [0,1,0,0,1,0,0,1],
    [0,1,0,0,0,0,0,1],
    [0,0,0,1,1,1,1,1],
    [0,0,0,0,0,0,0,1],
    [0,0,0,0,1,0,0,1],
    [0,0,0,0,1,0,0,0],
  ]
for index in range(8):
  leds[index] = Pin(leds[index],Pin.OUT)

def ligar(oqueFazer):
  for index in range(8):
    leds[index].value(oqueFazer[index])

while True:
  for index in range(10):
    ligar(nums[index])
    utime.sleep(0.7)


//Link do Wokwi:
https://wokwi.com/projects/373877550709754881
