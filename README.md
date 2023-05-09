# Emojis
# A bunch of emojis
# Its purpose is to entertain and the last face the the face that I made, the others were there automatically.
import simplegui
import math

# Global Variables

width = 600
height = 600
face1 = False
face2 = False
face3 = False
face4 = False
face5 = False

# Event Handlers

def all_false():
    global face1
    global face2
    global face3
    global face4
    global face5
    face1 = False
    face2 = False
    face3 = False
    face4 = False
    face5 = False
    
def toggle_face1():
    all_false()
    global face1
    face1 = not face1
    
def toggle_face2():
    all_false()
    global face2
    face2 = not face2
      
def toggle_face3():
    all_false()
    global face3
    face3 = not face3
    
def toggle_face4():
    all_false()
    global face4
    face4 = not face4

def toggle_face5():
    all_false()
    global face5
    face5 = not face5

def draw(canvas):
    if face1:
        canvas.draw_circle((width/2, height/2), width/2 - 50, 10, "Yellow", "Yellow")
        #eyes
        canvas.draw_circle((200, 200), 30, 5, "#7D5924", "#7D5924")
        canvas.draw_circle((395, 200), 30, 5, "#7D5924", "#7D5924")
        #mouth
        canvas.draw_circle((300, 360), 120, 5, "#7D5924", "#7D5924")
        canvas.draw_polygon([(80, 240), (450, 240), (450,370), (80,370)], 5, "yellow", "yellow")
        canvas.draw_polygon([(190, 385), (410, 385), (400,410), (200, 410)], 5, "white", "white")
        canvas.draw_line((180, 375), (420, 375), 5, "#7D5924")
        
    if face2:
        canvas.draw_circle((width/2, height/2), width/2 - 50, 10, "Yellow", "Yellow")
        #eyes
        canvas.draw_circle((200, 200), 30, 5, "#7D5924", "#7D5924")
        canvas.draw_circle((400, 200), 30, 5, "#7D5924", "#7D5924")
        
        #mouth
        canvas.draw_circle((300, 420), 110, 5, "#7D5924", "#7D5924")
        canvas.draw_circle((300, 440), 110, 5, "yellow", "yellow")
        
    if face3:
        canvas.draw_circle((width/2, height/2), width/2 - 50, 10, "#FA8072", "#FA8072")
        canvas.draw_circle([width/2.75, height/2 - 100], 10 , 10, "Black", "White")
        canvas.draw_circle([width - width/2.75, height/2 - 100], 10 , 10, "Black", "White")
        canvas.draw_line((width/3, height/2 - 150),(width/3 + 50, height/2 - 125), 5, "Black")
        canvas.draw_line((width - width/3, height/2 - 150),(width - width/3 - 50, height/2 - 125), 5, "Black")
        canvas.draw_polygon([(width/2, height - height/4), (width/2 - 50, height - height/4 + 25), (width/2 - 10, height - height/4 - 30), (width/2 + 10, height - height/4 - 30), (width/2 + 50, height - height/4 + 25)],10, "Black", "White")
        canvas.draw_line((width/2 - 30, height - height/4 - 10), (width/2 + 30, height - height/4 - 10), 5, "Black")

    if face4:
        canvas.draw_circle((300, 300), 250, 10, "#FCF4A3", "#FCF4A3")
        canvas.draw_circle((200, 200), 30, 2, "Black", "White")
        canvas.draw_circle((400, 200), 30, 2, "Black", "White")
        canvas.draw_circle((200, 215), 15, 2, "Black", "Black")
        canvas.draw_circle((400, 215), 15, 2, "Black", "Black")
        canvas.draw_circle((200, 215), 4, 2, "White", "White")
        canvas.draw_circle((400, 215), 4, 2, "White", "White")
        canvas.draw_line((160, 180),(200, 150), 3, "Black")
        canvas.draw_line((200, 150),(240, 180), 3, "Black")
        canvas.draw_line((360, 180),(400, 150), 3, "Black")
        canvas.draw_line((400, 150),(440, 180), 3, "Black")
        canvas.draw_circle((300, 400), 30, 2, "Black", "Black")
# the face i made (:
    if face5:
        canvas.draw_circle((width/2, height/2), width/2 - 50, 10, "Yellow", "Yellow")
        #mouth
        canvas.draw_circle((300, 340), 110, 5, "#7D5924", "#7D5924")
        canvas.draw_polygon([(250, 400), (350,400), (350, 460), (250, 460)], 5, "white", "white")
        canvas.draw_line((300,400), (300, 463), 4, "#7D5924")
        canvas.draw_circle((300, 290), 130, 5, "yellow", "yellow")
        #eyes
        canvas.draw_circle((200, 200), 90, 8, "black")
        canvas.draw_circle((400, 200), 90, 8, "black")
        canvas.draw_polygon([(150,100), (450, 100), (490, 150), (110, 150)], 5, "yellow", "yellow")
        canvas.draw_line((120,150), (480, 150), 8, "black")
        canvas.draw_polygon([(280, 150), (320, 150), (310, 170), (290,170)], 5, "black", "black")
        canvas.draw_circle((200, 200), 30, 5, "#7D5924", "#7D5924")
        canvas.draw_circle((390, 200), 30, 5, "#7D5924", "#7D5924")
        

        
frame = simplegui.create_frame("Pictures", width, height) 

frame.set_draw_handler(draw)
frame.add_button("Happy", toggle_face1, 100)
frame.add_button("Sad", toggle_face2, 100)
frame.add_button("Angry", toggle_face3, 100)
frame.add_button("Surprised", toggle_face4, 100)
frame.add_button("nerdy", toggle_face5, 100)

# Remember to start the frame
frame.start()
