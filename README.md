# Python-Calculator
Python calculator project. use tkinter library.
import tkinter
from tkinter import *

root = Tk()
root.title('My Python Calculator')
root.resizable(width = 0 ,height = 0)


#----------------------------------

add_text = StringVar()
x = 4
y = 1
bcol='gray'
fcol = 'black'
display = ''

#----------------------------------

def button_click (num):
    global display
    display = display + str(num)
    add_text.set(display)


def clear_button():
    global display
    display = ' '
    add_text.set(display)


def equal ():
    global display
    eq = str(round(eval(display),8))
    add_text.set(eq)
    display = eq

screen = Entry(root ,bd = 5, bg = 'white', width = 14,text = add_text , font = ('Times New roman',25,'bold'),fg = 'black')
button_7 = Button(root,text = '7',font = ('Times New roman',22,'bold'),bg = bcol ,width = x , height = y , fg = fcol, command = lambda:button_click(7))
button_8 = Button(root,text = '8', font = ('Times New roman',22,'bold'),bg = bcol ,width = x, height = y , fg = fcol, command = lambda:button_click(8))
button_9 = Button(root,text = '9', font = ('Times New roman',22,'bold'),bg = bcol ,width = x, height = y , fg = fcol, command = lambda:button_click(9))
button_4 = Button(root,text = '4', font = ('Times New roman',22,'bold'),bg = bcol ,width = x, height = y , fg = fcol, command = lambda:button_click(4))
button_5 = Button(root,text = '5', font = ('Times New roman',22,'bold'),bg = bcol ,width = x, height = y , fg = fcol, command = lambda:button_click(5))
button_6 = Button(root,text = '6', font = ('Times New roman',22,'bold'),bg = bcol ,width = x, height = y , fg = fcol, command = lambda:button_click(6))
button_1 = Button(root,text = '1', font = ('Times New roman',22,'bold'),bg = bcol ,width = x, height = y , fg = fcol, command = lambda:button_click(1))
button_2 = Button(root,text = '2', font = ('Times New roman',22,'bold'),bg = bcol ,width = x, height = y , fg = fcol, command = lambda:button_click(2))
button_3 = Button(root,text = '3', font = ('Times New roman',22,'bold'),bg = bcol ,width = x, height = y , fg = fcol, command = lambda:button_click(3))
button_0 = Button(root,text = '0', font = ('Times New roman',22,'bold'),bg = bcol ,width = x, height = y , fg = fcol, command = lambda:button_click(0))

button_plus = Button(root,text = '+', font = ('Times New roman',22,'bold'),bg = 'light green' ,width = x, height = y , fg = fcol,command = lambda:button_click('+'))
button_minus = Button(root,text = '-', font = ('Times New roman',22,'bold'),bg = 'light green' ,width = x, height = y , fg = fcol,command = lambda:button_click('-'))
button_multiply = Button(root,text = 'x', font = ('Times New roman',22,'bold'),bg = 'light green' ,width = x, height = y , fg = fcol,command = lambda:button_click('*'))
button_devide = Button(root,text = '/', font = ('Times New roman',22,'bold'),bg = 'light green' ,width = x, height = y , fg = fcol,command = lambda:button_click('/'))

button_equal = Button(root,text = '=', font = ('Times New roman',22,'bold'),bg = 'tomato' ,width = x, height = y , fg = fcol,command = lambda:equal())
button_clear = Button(root,text = 'C', font = ('Times New roman',22,'bold'),bg = 'orange' ,width = 9, height = y , fg = fcol,command = lambda:clear_button())
button_point = Button(root,text = '.', font = ('Times New roman',22,'bold'),bg = bcol ,width = x, height = y , fg = fcol, command = lambda:button_click('.'))


screen.grid(row = 0, column = 0, columnspan = 3,pady = 4)
button_7.grid(row = 1,column = 0,pady =3)
button_8.grid(row = 1,column = 1,pady =3)
button_9.grid(row = 1,column = 2,pady =3)
button_4.grid(row = 2,column = 0,pady =3)
button_5.grid(row = 2,column = 1,pady =3)
button_6.grid(row = 2,column = 2,pady =3)
button_1.grid(row = 3,column = 0,pady =3)
button_2.grid(row = 3,column = 1,pady =3)
button_3.grid(row = 3,column = 2,pady =3)
button_0.grid(row = 4,column = 1,pady =3)

button_plus.grid(row = 4,column = 0,pady =3)
button_minus.grid(row = 5,column = 0,pady =3)
button_multiply.grid(row = 4,column = 2,pady =3)
button_devide.grid(row = 5,column = 2,pady =3)

button_equal.grid(row = 5,column = 1,pady =3)
button_clear.grid(row = 6,column = 0,columnspan = 2, pady =3)
button_point.grid(row = 6,column = 2,pady =3)


root.mainloop()

