import pygame,sys
from pygame.locals import QUIT

pygame.init()
screen = pygame.display.set_mode((1000,1000))
pygame.display.set_caption("Shapes")
black = (0,0,0)
white = (255,255,255)
red = (255,0,0)
green = (0,255,0)
blue = (0,0,255)
screen.fill("white")
pygame.display.update()
while True:
    class Rect:
        def __init__(self,color,dimensions):
            self.rect_surf = screen
            self.rect_color = color
            self.rect_dimensions = dimensions
        def draw(self):
            self.draw_Rect = pygame.draw.rect(self.rect_surf, self.rect_color, self.rect_dimensions)
    class Circle:
        def __init__(self,color,position,radius):
            self.circle_surf = screen
            self.circle_color = color
            self.circle_position = position
            self.circle_radius = radius
        def draw(self):
            self.draw_Circle = pygame.draw.circle(self.circle_surf, self.circle_color, self.circle_position, self.circle_radius)
    class polygon:
        def __init__(self,color,points):
            self.polygon_surf = screen
            self.polygon_color = color
            self.polygon_points = points
        def draw(self):
            self.draw_polygon = pygame.draw.polygon(self.polygon_surf, self.polygon_color, self.polygon_points)



    greenRect=Rect(green,(50,20,100,100))
    redRect=Rect(red,(150,200,150,150))
    blueRect=Rect(blue,(300,400,200,200))

    greenCircle=Circle(green,(400,400),10)
    redCircle=Circle(red,(500,600),17)
    blueCircle=Circle(blue,(700,100),23)

    greenpolygon=polygon(green,[(700,200),(800,300),(900,700)])
    redpolygon=polygon(red,[(800,800),(800,900),(1000,1000)])
    bluepolygon=polygon(blue,[(400,700),(600,500),(750,750)])


    greenRect.draw()
    blueRect.draw()
    redRect.draw()
   
    greenCircle.draw()
    blueCircle.draw()
    redCircle.draw()

    greenpolygon.draw()
    redpolygon.draw()
    bluepolygon.draw()


    for event in pygame.event.get():
        if event.type == QUIT:
            pygame.quit()
            sys.exit()
    pygame.display.update()
