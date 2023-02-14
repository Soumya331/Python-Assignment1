Ans1) The key function for working with files in Python is the open() function. The open() function takes two parameters; filename, and mode.
There are four different methods (modes) for opening a file:
"r" - Read - Default value. Opens a file for reading, error if the file does not exist. Ex-: f = open("demofile.txt", "rt")r for read and t for text.
"a" - Append - Opens a file for appending, creates the file if it does not exist
"w" - Write - Opens a file for writing, creates the file if it does not exist
"x" - Create - Creates the specified file, returns an error if the file exists
In addition you can specify if the file should be handled as binary or text mode
"t" - Text - Default value. Text mode
"b" - Binary - Binary mode (e.g. images)

Ans2) The close() method closes an open file ans it is important because in some cases, due to buffering, changes made to a file may not show until you close the file.

Ans3)
```python
file = open("file.txt", "wt")
```


```python
file.write('I want to become a data scientist')
file.close()
```


```python
file = open("file.txt", "rt")
```


```python
file.read()
```




    'I want to become a data scientist'



Ans4) read(): The read() method returns the whole text, but you can also specify how many characters you want to return
readline(): Python readline() method will return a line from the file when called
readlines(): readlines() method will return all the lines in a file in the format of a list where each element is a line in the file


```python
file1 = open("file1.txt", "wt")
lines = ('I want to become a data scientist\n', 'I will become a data scientist\n')
file1.writelines(lines)
file1.close()
```


```python
file1 = open("file1.txt","rt")
```


```python
file1.read()
```




    'I want to become a data scientist\nI will become a data scientist\n'




```python
file1 = open("file1.txt","rt")
ex= file1.readlines()
print(ex)
```

    ['I want to become a data scientist\n', 'I will become a data scientist\n']



```python
file1 = open("file1.txt","rt")
ex= file1.readline()
print(ex)
```

    I want to become a data scientist
    


Ans5) The with statement works with the open() function to open a file.
The advantage of using with statement: Unlike open() where you have to close the file with the close() method, the with statement closes the file for you without you telling it to. This is because the with statement calls 2 built-in methods behind the scene – enter() and exit() .

Ans6) The write() function will write the content in the file without adding any extra characters.
writelines() function writes the content of a list to a file in new lines.


```python
file1 = open("file2.txt", "wt")
lines = ('I want to become a data scientist\n', 'I will become a data scientist\n')
file1.writelines(lines)
file1.close()
```


```python
file1 = open("file2.txt","rt")
file1.read()
```




    'I want to become a data scientist\nI will become a data scientist\n'




```python
file = open("file3.txt", "wt")
file.write('I want to become a data scientist')
file.close()
```


```python
file = open("file3.txt", "rt")
file.read()
```




    'I want to become a data scientist'




```python

```

