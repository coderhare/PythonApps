# Text Editor

This porgram is a GUI text editor which now just has simple functions:

- Edit texts, save it and open it with its name.

It was originally the code of `Beginning Python From Novice to Professional(Third Edtion)`,and I hope to improve it in with deeper study of Python.

```python
from tkinter import *
from tkinter.scrolledtext import ScrolledText

def load():
  with open(filename.get()) as file:
    	contents.delete('1.0', END)
      contents.insert(INSERT, file.read())

def save():
  with open(filename.get(), 'w') as file:
    file.write(contents.get('1.0', END))
 
top = Tk()
top.title("Simple Editor")

contents = ScrolledText()
contents.pack(side=BOTTOM, expand=True, fill=BOTH)

filename = Entry()
filename.pack(side=LEFT, epand=True, fill=BOTH)

Button(text='Open', command=load).pack(side=LEFT)
Button(text='Save', command=save).pack(side=LEFT)

mainloop()
```

![image-20210305205215072](/Users/wocaibujiaoquanmei/Library/Application Support/typora-user-images/image-20210305205215072.png)

