import random
import string
import tkinter as tk

def generate_password(charlong):
    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(characters) for _ in range(charlong))
    return password

def generate_password_interface():
    try:
        charlong_password = int(entry_charlong_password.get())
        if charlong_password < 6:
            label_result.config(text="Parola uzunluğu 6 dan büyük olmalıdır.")
        else:
            password_generate = generate_password(charlong_password)
            label_result.config(text="Parola: " + password_generate)
    except ValueError:
        label_result.config(text="Geçersiz giriş. Parola uzunluğu bir sayı olmalıdır.")

root = tk.Tk()
root.title("parola oluşturucu")

label_long = tk.Label(root, text="Parola uzunluğu: ")
label_long.pack()

entry_charlong_password = tk.Entry(root)
entry_charlong_password.pack()

button_generate = tk.Button(root, text="parola oluştur ", command=generate_password_interface)
button_generate.pack()

label_result = tk.Label(root, text="")
label_result.pack()

root.mainloop()
