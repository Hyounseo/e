[log.py](https://github.com/user-attachments/files/22038835/log.py)
import tkinter as tk

def login():
    user_id = id_entry.get()
    user_pw = pw_entry.get()
    
    print(f"ID: {user_id}")
    print(f"PW: {user_pw}")
    
root = tk.Tk()
root.title("로그인")


id_label = tk.Label(root, text="ID:")
id_label.grid(row=0, column=0, padx=5, pady=5, sticky="e")
id_entry = tk.Entry(root)
id_entry.grid(row=0, column=1, padx=5, pady=5)


pw_label = tk.Label(root, text="PW:")
pw_label.grid(row=1, column=0, padx=5, pady=5, sticky="e")
pw_entry = tk.Entry(root, show="*") 
pw_entry.grid(row=1, column=1, padx=5, pady=5)


login_button = tk.Button(root, text="로그인", command=login)
login_button.grid(row=2, columnspan=2, padx=5, pady=10)


root.mainloop()
