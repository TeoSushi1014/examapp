# Multiple Choice Test Application Development Guide

## Application Description

This application manages and processes multiple choice tests. Each question in the test includes the following components:
- **Question content**
- **Answer A content**
- **Answer B content**
- **Correct answer** (A or B)

The application has the following main functions:
1. **Create multiple choice tests** with multiple questions, input from keyboard and save to `*.TTN` file format.
2. **Read `*.TTN` file content** for users to take the test.
3. **Read a `*.TTN` file** and remove excess whitespace in questions and answers, then overwrite the original file.
4. **Check if two questions are identical.**

## Methods and Functions

### 1. **`CauhoiTN` Class**

The `CauhoiTN` class has the following properties and methods:

#### Properties
- **noidung**: Question content.
- **dapAnA**: Answer A content.
- **dapAnB**: Answer B content.
- **dapAnDung**: Correct answer (A or B).

#### Methods
- **`nhap()`**: Input question data from keyboard, including question content, answer A, answer B, and correct answer.
- **`docfile(ifstream& f)`**: Read question from file stream `f` and save to corresponding properties.
- **`ghifile(ofstream& f)`**: Write question content to file stream `f`.
- **`kiemtra()`**: Display question and allow user to input answer. The method checks if the answer is correct and displays the result.
- **`xuat()`**: Output question to screen, including question content, answers A, B, and correct answer.
- **`giongnhau(CauhoiTN cau1, CauhoiTN cau2)`**: Function to check if two questions are identical, using the `friend` keyword.

### 2. **Menu**
The application will have a menu for users to select the following functions:
- Create new multiple choice test from keyboard and save to file.
- Read test from file and allow users to take the test.
- Read and edit file to remove excess whitespace.
- Check if questions are identical.
- Exit program.

### 3. **Main Functions**
1. **Create multiple choice test:**
   - Users can input multiple choice questions from keyboard. Each question will include question content, answers A, B, and correct answer.
   - These questions will be saved to a file with `*.TTN` format.

2. **Read content from file and take test:**
   - Users can select an existing test from a `*.TTN` file. Questions will be read and displayed for users to take the test.
   - Users will input answers and the application will check their responses.
   
3. **Edit test file:**
   - This function allows users to read a `*.TTN` file and remove excess whitespace in questions and answers.
   - After removing excess whitespace, the file will be overwritten with new content.

4. **Check for identical questions:**
   - The `giongnhau()` function will check if two questions are identical, based on question content, answer A, answer B, and correct answer.

## Development Requirements

1. **Create `CauhoiTN` class** with properties and methods described above.
2. **Build menu** allowing users to select functions, including:
   - Create new test.
   - Read file and take test.
   - Edit file (remove excess whitespace).
   - Check for identical questions.
   - Exit program.
3. **Write `giongnhau(CauhoiTN cau1, CauhoiTN cau2)` function** to check if questions are identical, using the `friend` keyword.

## Notes

- **Students need to submit 2 files**:
  1. **Screenshot file** showing application execution, displaying results after user inputs questions, takes test, and checks answers.
  2. **Compressed source code file** of the project to submit to instructor.

- **Student information**: First line of the program needs to print student information (Student ID and Full Name) when starting the program.

## Application Development Steps

1. **Design `CauhoiTN` class**:
   - Class properties and methods will help manage and process multiple choice questions.
   - This class must have methods for input, file reading and writing, answer checking, and question display.

2. **Build menu**:
   - Menu will include functions for users to select such as creating tests, reading and taking tests, editing test files, and checking for identical questions.

3. **File checking and editing**:
   - Need to ensure that `*.TTN` files can be read, edited (remove excess whitespace), and saved correctly.

4. **Application testing**:
   - After development, need to test application to ensure all functions work correctly, including checking for identical questions and checking correct/incorrect answers.

5. **Prepare submission**:
   - Take screenshots while application is running, including question input process, test taking, and result checking.
   - Compress all project source code into a file and submit along with screenshot file.

## Conclusion

This application will help manage and process multiple choice questions, allowing users to create, edit, and take tests easily. Functions such as checking correct/incorrect answers and checking for identical questions will make the application useful and effective for users. 