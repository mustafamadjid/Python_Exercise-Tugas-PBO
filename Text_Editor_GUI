import tkinter as tk
from tkinter import filedialog

#Init
window = tk.Tk()
window.configure(bg="white")
window.minsize(1000,800)
window.title("Text Editor")

#Frame  
frame1 = tk.Frame(window)
frame2 = tk.Frame(window)
frameButton = tk.Frame(frame1)


frame1.pack(fill="both", expand=True, side="left")
frame2.pack(fill="both", expand=True, side="left")
frameButton.pack(side="top",fill="x")



#Method
def open_file():
    text_file = filedialog.askopenfilename(filetypes=[("Text Files", "*.txt")])
    if text_file:
        with open(text_file, "r") as file:
            text_widget.delete("1.0", tk.END)
            text_widget.insert(tk.END, file.read())

def save_file():
    text_file = filedialog.asksaveasfilename(defaultextension=".txt", filetypes=[("Text Files", "*.txt")])
    if text_file:
        with open(text_file, "w") as file:
            file.write(text_widget.get("1.0", tk.END))

# Button and Widget

open_button = tk.Button(frameButton, text="Open Text File",height=2, command=open_file)
open_button.pack(fill="x", expand=True,pady=20)

save_button = tk.Button(frameButton, text="Save Text File",height=2, command=save_file)
save_button.pack(fill="x", expand=True,pady=20)

close_button = tk.Button(frameButton,command=window.destroy,height=2,text="Close")
close_button.pack(fill="x", expand=True,pady=20)

text_widget = tk.Text(frame2, wrap=tk.WORD, font=("Fira Code", 12),width=800)
text_widget.pack(fill="both", expand=True)

window.mainloop()
