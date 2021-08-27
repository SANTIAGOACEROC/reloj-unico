reloj

vertical_position = 0
vertical_position1 = 0
vertical_position2 = 0
def setup():
    size(600, 250)
    background(10)
def draw():
    global vertical_position
    global vertical_position1
    global vertical_position2
    background (map(second(), 0, 59, 250, 0))
    noStroke()
    if vertical_position > height:
        vertical_position = 0
    else:
        vertical_position = map(second(), 0, 59, 0, height)
        
    if vertical_position1 > height:
        vertical_position1 = 0
    else:
        vertical_position1 = map(minute(), 0, 59, 0, height)
        
        
    if vertical_position2 > height:
        vertical_position2 = 0
    else:
        vertical_position2 = map(hour(), 0, 23, 0, height)
    stroke(0)
    fill(255,100,30)
    ellipse(300, vertical_position1, 55, 55)
    fill(40,92,152)
    square(150, vertical_position2, 55)
    fill(35,247,72)
    ellipse(450, vertical_position, 55, 55)