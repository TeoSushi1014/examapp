# Multiple Choice Exam Application

## Project Description

This application manages and processes multiple-choice exams. Each question in the exam includes:
- Question content
- Answer A content
- Answer B content
- Correct answer (A or B)

## Main Features

1. **Create Multiple Choice Exams**
   - Create new exams with multiple questions
   - Input from keyboard
   - Save to `*.TTN` format files

2. **Read and Take Exams**
   - Read exam content from `*.TTN` files
   - Allow users to take the exam
   - Check and display results

3. **File Processing**
   - Read `*.TTN` files
   - Remove excess whitespace from questions and answers
   - Save changes back to the original file

4. **Question Comparison**
   - Check if two questions are identical
   - Compare based on content, answers, and correct answer

## Technical Details

### `CauhoiTN` Class (Question Class)

#### Properties
- `noidung`: Question content
- `dapAnA`: Answer A content
- `dapAnB`: Answer B content
- `dapAnDung`: Correct answer (A or B)

#### Methods
- `nhap()`: Input question from keyboard
- `docfile()`: Read question from file
- `ghifile()`: Write question to file
- `kiemtra()`: Check user's answer
- `xuat()`: Display question
- `giongnhau()`: Compare two questions for similarity

## Development Requirements

1. **Required Files for Submission**
   - Screenshot of application execution
   - Source code archive

2. **Student Information**
   - Display student ID and name at program start

## How to Use

1. Run the application
2. Choose from the menu options:
   - Create new exam
   - Read and take exam
   - Edit exam file (remove excess whitespace)
   - Check for duplicate questions
   - Exit program

## Development Guidelines

1. **Class Implementation**
   - Implement `CauhoiTN` class with all required properties and methods
   - Ensure proper file handling for `*.TTN` format

2. **Menu System**
   - Implement user-friendly menu interface
   - Handle all user inputs appropriately

3. **File Operations**
   - Implement proper file reading and writing
   - Handle whitespace removal correctly

4. **Testing**
   - Test all features thoroughly
   - Verify correct answer checking
   - Ensure proper duplicate question detection

## Note

For Vietnamese version, please refer to [DEVELOPMENT.vi.md](DEVELOPMENT.vi.md) 