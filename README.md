from tkinter import *
import random
root = Tk()
root.geometry('200x200')
root.title("strong password")
def f():
    n=e.get()
    s=''
    characters = [
        'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z',  
        'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z',  
        '0', '1', '2', '3', '4', '5', '6', '7', '8', '9',  
        '!', '@', '#', '$', '&', '_'  
    ]
    for i in range(int(n)):
        a=random.choice(characters)
        s+=a
    lb.insert(0, s)



lbl = Label(root,text='كم طول الكلمة؟؟',font='Arial 15')
lbl.pack()
e= Entry(root,font='Arial 15',bd=7)
e.pack()
b=Button(root,text='انشاء',command=f,height=1,width=7,font=8,bg='silver')
b.pack()
lb1 = Label(root,text='-:الكلمة ',font='Arial 15')
lb1.place(x=50,y=100)
lb = Entry(root,font='Arial 15')
lb.place(x=0,y=130)
root.mainloop()
