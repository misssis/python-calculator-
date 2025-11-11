# python pasword maker -
this is a calculator this code was made by a beginner , so please bear this in mind   
import tkinter as tk  
import sys 
from tkinter.ttk import Label

def making_a_password(): 
 user = entry.get()
 messages = []
 number= ('1','2','3','4','5','6','7','8','9','0')
 if any (c in number for c in user ):
  my_label1 = Label(text='correct use of numbers ')
  my_label1.pack()
 
 else : 
  my_label7 = Label(text='pleas use numbers ')
  my_label7.pack()

 specia_characters= ('!','@','#','$','%','^','&','*','(',')','-','+','?','_','=','<>','/',)
 if any (c in specia_characters for c in user ):
  my_label2 = Label(text='correct use of special charcatrers ')
  my_label2.pack()
 else: 
   my_label9 = Label(text='please use special characters  ')
   my_label9.pack()

 password= user 

 len((user))

 if len((user))>8: 
    my_label3 = Label(text='correct number of characters  ')
    my_label3.pack()


 else : 
   print ('please chaeck for more than 8 charcaters , use of special charcaters and use of numbers ')


   
root = tk.Tk()
root.geometry('400x400')

Label1=Label(root , text='password maker', font=('Arial',30))
Label1.pack()

l2=Label(root,text='please ente the password ', font=('Arial',10))
l2.pack()

entry=tk.Entry(root,width=20)
entry.pack()

b1=tk.Button(root, text='enter',command= making_a_password)
b1.pack()

output_label = tk.Label(root, textvariable=making_a_password)
output_label.pack(pady=10)

clear_button = tk.Button(root, text="Clear Entry", font=("Helvetica", 14))
clear_button.pack(pady=20)

clear_button.config(command=lambda: entry.delete(0, tk.END))


root.mainloop()
