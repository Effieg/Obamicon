# Obamicon
from Myro import *
from Graphics import *

picture = makePicture("effie.png")
show(picture)


Obama_DarkBlue = makeColor(0,51,76)
Obama_Red = makeColor(217, 26, 33)
Obama_Blue = makeColor(112,150,158)
Obama_Yellow = makeColor(252, 227, 166)

for pixel in (getPixels(picture)):
    r=getRed(pixel)
    g=getGreen(pixel)
    b=getBlue(pixel)
    grayValue = .2126*r+.7152*g+.0722*g
    if grayValue > 180:
        setColor(pixel, Obama_Yellow)
    elif grayValue > 120:
        setColor(pixel, Obama_Blue)
    elif grayValue > 60:
        setColor(pixel, Obama_Red)
    else:
        setColor(pixel, Obama_DarkBlue)
        
