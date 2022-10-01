from tkinter import *
import sqlite3
root = Tk()
root.config(bg="black")
root.title("from to input data")
root.geometry('500x500')
e1 = StringVar()
e2 = StringVar()
var = IntVar()
c = StringVar()
Var1 = IntVar()
#=================
def insert_database():
    name1 = e1.get()
    email = e2.get()
    gender = var.get()
    country = c.get()
    programming = Var1.get()
    conn = sqlite3.connect("form.db")
    with conn:
        cursor = conn.cursor()
        cursor.execute("CREATE TABLE IF NOT EXISTS student (funllname text,email text,gender text,country text,programming text)")
        cursor.execute("insert INTO student(funllname,email,gender,country,programming) values(?,?,?,?,?)",(name1,email,gender,country,programming))
        conn.commit()
#----------------------------

def delete_database():
    name1 =e1.get()
    email = e2.get()
    gender = var.get()
    country =c.get()
    programmingm =Var1.get()
    conn =sqlite3.connect("from.db")
    with conn:
        cursor =conn.cursor()
        cursor.execute('delete from student where funllname=? and email=? and gender=? and country=? and programming=?',(name1,email,country,gender,programmingm))
    conn.commit()
    #==============================
Label(root, text="reqestration from",width=20,fg='red',font=("bold",20)).place(x=90, y=53)
Label(root, text="fullname",width=20,font=("bold",10)).place(x=80, y=130)
Entry(root,textvar=e1).place(x=250,y=130)
Label(root,text="email",width=20, font=("bold",10)).place(x=68, y=180)
Entry(root,textvar=e2).place(x=250, y=180)
#نوع بيانات الادخال
var = IntVar()

Label(root,text="gender", width=20, font=("bold", 10)).place(x=65, y=230)
Radiobutton(root,text="male",padx=3,variable=var,value=1).place(x=235,y=230)
Radiobutton(root,text="famle",padx=15,variable=var,value=2).place(x=290,y=230)
list1=["canda","india","Uk","yemen"]
c=StringVar()
#================
droplist = OptionMenu(root, c, *list1)
droplist.config(width=18)
c.set("select the county")
droplist.place(x=250,y=280)
Label(root,text="programming",width=20,font=("bold,10")).place(x=85, y=330)
var=IntVar()
#===============
Checkbutton(root, text="java", variable=Var1).place(x=280,y=330)
Checkbutton(root, text="python", variable=Var1).place(x=350,y=330)
Button(root,text="insert",width=20, bg='brown',fg="white",command=insert_database).place(x=180,y=390)
Button(root,text="delete",width=20, bg='brown',fg="white",command=delete_database).place(x=180,y=450)
root.mainloop()
