## Exercise: Analyzing Weather Data

In this exercise, you will analyze weather data for a week. The data includes daily temperatures and humidity levels. You will perform various tasks such as reading data from a file, calculating average values, finding maximum and minimum values, and handling potential errors using try-except blocks.

### Part 1: Prepare the Data

1. **Create a Text File**:
   - Name the file `weather_data.csv`.
   - Add the following content to the file:

     ```
     Day, Temperature, Humidity
     Monday,25,60
     Tuesday,30,65
     Wednesday,28,62
     Thursday,26,61
     Friday,27,63
     Saturday,29,64
     Sunday,24,59
     ```

### Part 2: Read the Data from the File

2. **Open and Read the File**:
   - Write a function to read the data from the file.
   - Store the data in a list of dictionaries.
   - Each dictionary should have keys: `day`, `temperature`, and `humidity`.
   - Use try-except blocks to handle potential file-related errors.

### Part 3: Calculate Average Temperature and Humidity

3. **Average Calculation**:
   - Write a function to calculate the average temperature.
   - Write another function to calculate the average humidity.
   - Use numpy arrays to facilitate these calculations.

### Part 4: Find Maximum and Minimum Values

4. **Maximum and Minimum Calculation**:
   - Write a function to find the day with the maximum temperature and its value.
   - Write a function to find the day with the minimum temperature and its value.
   - Write functions to find the days with the maximum and minimum humidity and their values.

### Part 5: Handle Errors Gracefully

5. **Error Handling**:
   - Modify the function that reads the weather data to handle errors such as missing or malformed data lines.
   - Use try-except blocks to catch and report these errors without stopping the execution of the program.

### Summary

- **Lists**: Use to store the weather data.
- **Dictionaries**: Each entry in the list should be a dictionary representing a day's data.
- **Numpy Arrays**: Use to calculate the average values.
- **Try-Except Blocks**: Use to handle file not found and data parsing errors.
- **Functions**: Encapsulate logic for reading data, calculating averages, and finding min/max values.
- **File Operations**: Open and read from the weather data file.
- **Loops**: Iterate over file lines and data entries.

### Additional Tips

- Make sure to import necessary modules like `numpy`.
- Test your functions individually to ensure they work correctly.
- Print intermediate results to verify your calculations step by step.
- Handle edge cases, such as empty files or files with incorrect data formats.
