# Calculator-python-project
import tkinter
from tkinter import *
root=Tk()
root.title("My Calculator")
root.geometry("570x600+100+200")
root.resizable(False,False)
root.configure(bg='#17161b')
eq=""
def show(val):
    global  eq
    eq+=val
    result.config(text=eq)

def clear():
    global eq
    eq=""
    result.config(text=eq)

def calculate():
    global eq
    res=""
    if eq!="":
        try:
            res=eval(eq)
        except:
            res="Error"
            eq=""
    result.config(text=res)



result=Label(root,width=25,height=2,text="",font=("arial",30))
result.pack()
#first row buttons
Button(root,text="C",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='red',command=lambda: clear()).place(x=10,y=100)
Button(root,text="/",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("/")).place(x=150,y=100)
Button(root,text="%",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("%")).place(x=290,y=100)
Button(root,text="*",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("*")).place(x=430,y=100)

#second row buttons
Button(root,text="7",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("7")).place(x=10,y=185)
Button(root,text="8",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("8")).place(x=150,y=185)
Button(root,text="9",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("9")).place(x=290,y=185)
Button(root,text="+",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("+")).place(x=430,y=185)

#third row buttons
Button(root,text="6",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("6")).place(x=10,y=270)
Button(root,text="5",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("5")).place(x=150,y=270)
Button(root,text="4",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("4")).place(x=290,y=270)
Button(root,text="-",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("-")).place(x=430,y=270)

#fourth row buttons
Button(root,text="3",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("3")).place(x=10,y=355)
Button(root,text="2",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("2")).place(x=150,y=355)
Button(root,text="1",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("1")).place(x=290,y=355)
Button(root,text="=",width=5,height=3,font=('arial',30,'bold'),bd=1,fg='#fff',bg='orange',command=lambda: calculate()).place(x=430,y=355)

#fifth row buttons
Button(root,text="0",width=11,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show("0")).place(x=10,y=440)
Button(root,text=".",width=5,height=1,font=('arial',30,'bold'),bd=1,fg='#fff',bg='#2a2d36',command=lambda: show(".")).place(x=290,y=440)


root.mainloop()
