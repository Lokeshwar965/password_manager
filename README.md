Source Code:
import tkinter as tk
from tkinter import messagebox

# Function to handle sign up button click event
def sign_up():
    username = username_entry.get()
    password = password_entry.get()
    
    # Save the username and password to a file or database
    # Here, we are just displaying a message box
    messagebox.showinfo("Password Manager", "Sign up successful!")

# Function to handle login button click event
def login():
    username = username_entry.get()
    password = password_entry.get()
    
    # Check if the username and password match the stored credentials
    # Here, we are just displaying a message box
    messagebox.showinfo("Password Manager", "Login successful!")

# Function to handle exit button click event
def exit_program():
    window.destroy()

# Create the main window
window = tk.Tk()
window.title("Password Manager")

# Create labels and entry fields
username_label = tk.Label(window, text="Username:")
username_label.pack()
username_entry = tk.Entry(window)
username_entry.pack()

password_label = tk.Label(window, text="Password:")
password_label.pack()
password_entry = tk.Entry(window, show="*")
password_entry.pack()

# Create buttons
sign_up_button = tk.Button(window, text="Sign up", command=sign_up)
sign_up_button.pack()

login_button = tk.Button(window, text="Login", command=login)
login_button.pack()

exit_button = tk.Button(window, text="Exit", command=exit_program)
exit_button.pack()

# Start the main event loop
window.mainloop()
