from tkinter import *
import tkinter as tk
from os import *
import os

file = ficheiro
mkdir(f'C:\\{file}', True)

def in_file():
    arquivos = pasta
    mkdir(f'C:\\{file}\\{arquivos}')
    print("Deseja parar?\n 1-Sim\n 2-Não")
    stop = int(input(">"))
    if stop == 1:
        exit()
    else:
        pass

root = tk.Tk()
root.title("File creator")
root.geometry("500x500+500+500")
root.wm_resizable(width=False, height=False)
root.config(bg="#ffffff")

Label1 = tk.Label(root, text="Nome da pasta", command=in_file font="Time 10")
Label1.place(height=20, width=200, x=25, y=100)

pasta = Entry(root, font= "Arial 10 italic")
pasta.place(x=200, y=100)

Label2 = tk.Label(root, text="Nome do(s) arquivo(s)", font="Time 10")
Label2.place(height=20, width=200, x=25, y=200)

ficheiro = Entry(root, font= "Arial 10 italic")
ficheiro.place(x=200, y= 200)

Confirm = tk.Button(root, text="Confirmar", font="Time 10")
Confirm.place(x=375, y=100)

root.mainloop()

