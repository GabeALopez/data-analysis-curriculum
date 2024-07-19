# Opening and Closing Files

We need to be able to use files to be able to start doing the actual analysis part in data analysis and there are many files types out there that you may get. The common ones are excel(.xls), text files (.txt), or CSV files (.csv). You will get .csv files most of the time though as it an easy way for most people to format data in a simple and expandable form. I am going to focus on csv files as, again, they are the most common type you will come across. So how do we open a .csv file? There are two main ways to do it. Either through default libraries (which I don't recommend) or through Pandas. I am going to start with the default library way, just so if you can't use/import pandas for some reason.  

Alright so in order to import a csv file we need to import the csv default module that comes with python. I'll explain what everything is (keywords, lines, etc) after the example below. But anyways after that we are going to use two keywords 'with' and 'open'. Following this, we need to tell python the file path, what mode to read the file in, and what is a new line in the file. This is the general header to open a csv file. But this doesn't really mean anything if we don't see the code. Let's show some code:

```python
import csv

def read_csv_skip_header(file_path):
    data = []
    try:
        with open(file_path, mode='r', newline='') as file:
            csv_reader = csv.reader(file)
            next(csv_reader)  # Skip the header row
            for row in csv_reader:
                data.append(row)
        return data
    except FileNotFoundError:
        print(f"The file at {file_path} was not found.")
    except Exception as e:
        print(f"An error occurred: {e}")

# Usage example
file_path = 'example.csv'
data = read_csv_skip_header(file_path)
print("Data:", data)
```
As we can see the script first starts with importing the csv module where we can start to use the functions that are inside that module. After that, we can later see the 'with open' keywords where 'open' is being supplied with 3 parameters. One is the file path, second the mode (in this case read mode), and third the newline (which tells python what counts as a newline in csv file). Really after this you are starting to read the actual data in the file. We use the 'reader. function in the 'csv' module to read the file as a csv file. The next line uses the 'next' function which skips the first line where column headers are. Finally we are looping through each row of the csv file and sending that data into data structure. 

Once all that is done, we have imported the file into a data structure for use to use later in the code. Some added info I wanted to add here is about 'with' and 'open'. 'with' is a keyword in python that tells python to only open the file within the context of the coding running underneath it. Once the code underneath it executes, python will close the file. 'open' is a function in python dedicated to, you guessed it, opening files but what is special about it are the params that are being fed to this function to do the function it needs to do (no pun intended)