# Login_page# importing all files from tkinter
from tkinter import *
from functools import partial
 # defining a function to check the login is valid or not
def validLogin():
    
    print("Username Entered:", username.get())
    print("Password Entered:", password.get())
    
# Creating a gui window
root = Tk()

# Giving the dimensions of the window
root.geometry('600x300')

# Giving title to the window
root.title('Form Of Hell!')

# creating usernameLabel and text box
userLabel = Label(root, text = 'Guilty Name').grid(row=0, column=0)
username = StringVar()
userEntry = Entry(root, textvariable = userLabel).grid(row=0, column=1)

# creating passwordLabel and textbox
passLabel = Label(root, text = 'Guilty\'s Crime').grid(row=1, column=0)
password = StringVar()
passEntry = Entry(root, textvariable = passLabel, show = '*').grid(row=1, column=1)

#calling the validLogin function
validLogin = partial(validLogin, username, password)

# Creating a login button
loginButton = Button(root, text = 'Click To Enter In Guilty In Hell!', command = validLogin).grid(row=4, column=0)

root.mainloop()

