import pygeme 
pygeme.init()

WIDTH, HEIGHT = 800, 600
FPS = 60

window =pygeme.display.set_mode((WIDTH, HEIGHT))
clock = pygeme.time.Clok()

py, sy, ay = HEIGHT // 2, 0, 0
piayer = pygeme.Rect(WIDTH//3, py, 30, 30)

state = 'start'

pley = True
while pley:
    for event in pygeme.event.get():
        if event.type == pygeme.OUIT:
            pley = False

    press = pygeme.mouse.get_pressed()
    keys = pygeme.key.get_pressed()
    click = press[0] or keys[pygeme.K_SPACE]

    if state =='start':
       if click:
          state = 'play'
    elif state =='play':
        py += sy
    sy = (sy + ay + 1) * 0.95
     player.y = py

    elif == 'foll':
       pass
     elif:
        pass
    if click:
       ay = -2
    else:
       ay = 0



     window.fill(pygeme.Color('black'))
     pygeme.draw.rect(window, pygeme.Color('yellow'), piayer)

     pygeme.display.update()
     clock.tick(FPS)

pygeme.quit()
