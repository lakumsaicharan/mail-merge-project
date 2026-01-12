# ✉️ Mail Merge Project

An automated mail merge system built with Python that generates personalized letters from a template and a list of names. Perfect for creating custom invitations, letters, or any bulk personalized correspondence efficiently!

## 📋 Description

This project automates the tedious task of creating multiple personalized documents from a single template. By reading names from a text file and a letter template, the program automatically generates individual letters with each recipient's name, saving time and reducing manual errors. It's an excellent example of automation in action and demonstrates practical file handling in Python.

## ✨ Features

- 📄 **Template-Based Generation**: Uses a customizable letter template
- 📃 **Bulk Processing**: Processes multiple names from a file
- 🖄️ **Personalization**: Replaces placeholder with actual names
- 💾 **Automatic Saving**: Saves each letter as a separate file
- 📁 **Organized Output**: Stores generated letters in a dedicated folder
- ⚡ **Fast Processing**: Handles large lists efficiently
- 📝 **Clean Output**: Professional-looking personalized letters
- 🛠️ **Reusable**: Easily modify template and names for different purposes

## 🛠️ Technologies Used

- **Python 3.x**
- **File I/O**: Reading and writing text files
- **String Manipulation**: Text replacement and formatting
- **Path Management**: Directory and file handling

## 📁 Project Structure

```
mail-merge-project/
│
├── Mail Merge Project Start/
│   ├── Input/
│   │   ├── Names/
│   │   │   └── invited_names.txt       # List of recipient names
│   │   └── Letters/
│   │       └── starting_letter.txt    # Letter template
│   └── Output/
│       └── ReadyToSend/               # Generated letters appear here
├── main.py                           # Main script
├── LICENSE                           # MIT License
└── README.md                         # Project documentation
```

## 🚀 Installation & Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/lakumsaicharan/mail-merge-project.git
   cd mail-merge-project
   ```

2. **Ensure Python is installed**:
   ```bash
   python --version
   ```
   *Note: Python 3.x is required*

3. **No additional dependencies needed** - Uses only Python standard library!

## 📚 Usage

### Step 1: Prepare Your Names List
Edit `Input/Names/invited_names.txt` with one name per line:
```
John
Mary
David
Sarah
```

### Step 2: Customize Your Letter Template
Edit `Input/Letters/starting_letter.txt` with your message:
```
Dear [name],

You are invited to my birthday party on Saturday.

Hope you can make it!

Best regards,
Your Name
```

### Step 3: Run the Script
```bash
python main.py
```

### Step 4: Collect Your Letters
Find personalized letters in `Output/ReadyToSend/` folder!
- `letter_for_John.txt`
- `letter_for_Mary.txt`
- `letter_for_David.txt`
- `letter_for_Sarah.txt`

## 💡 How It Works

### The Magic Behind Mail Merge

1. **Read Names**: Program reads all names from `invited_names.txt`
2. **Load Template**: Reads the letter template from `starting_letter.txt`
3. **Replace Placeholder**: For each name, replaces `[name]` with the actual name
4. **Save Individual Letters**: Creates a separate file for each person
5. **Organize Output**: Stores all letters in the `ReadyToSend` folder

### Code Flow
```python
# Read all invited names
with open("Input/Names/invited_names.txt") as names_file:
    names = names_file.readlines()

# Read letter template
with open("Input/Letters/starting_letter.txt") as letter_file:
    letter_contents = letter_file.read()

# Generate personalized letters
for name in names:
    stripped_name = name.strip()
    new_letter = letter_contents.replace("[name]", stripped_name)
    
    # Save each letter
    with open(f"Output/ReadyToSend/letter_for_{stripped_name}.txt", mode="w") as completed_letter:
        completed_letter.write(new_letter)
```

## 🎓 Learning Objectives

This project demonstrates:
- ✅ File I/O operations (reading and writing)
- ✅ String manipulation and replacement
- ✅ List iteration and processing
- ✅ Path and directory management
- ✅ Automation of repetitive tasks
- ✅ Template-based document generation
- ✅ Practical application of Python basics

## 🎯 Use Cases

### Personal
- 🎉 Birthday party invitations
- 💌 Wedding invitations
- 🎄 Holiday greeting cards
- 📧 Thank you letters

### Professional
- 💼 Job application cover letters
- 📨 Marketing email campaigns
- 📄 Certificate generation
- 📢 Event announcements
- 📊 Sales proposals
- 📩 Customer notifications

## 🔧 Customization Ideas

### Multiple Placeholders
Extend to replace multiple fields:
```
Dear [name],

Your appointment is scheduled for [date] at [time].
Location: [address]

See you soon!
```

### Email Integration
Add SMTP functionality to send emails automatically:
```python
import smtplib
# Send generated letters via email
```

### CSV Support
Read from CSV files for more complex data:
```python
import csv
# Handle multiple columns of data
```

### PDF Generation
Convert letters to PDF format:
```python
from reportlab.pdfgen import canvas
# Generate PDF letters
```

## 📈 Possible Enhancements

**Future Features:**
- [ ] GUI interface for easier use
- [ ] Support for multiple templates
- [ ] CSV/Excel file support
- [ ] Email sending capability
- [ ] PDF output option
- [ ] Rich text formatting
- [ ] Preview before generating
- [ ] Undo/redo functionality
- [ ] Progress bar for large batches

## ⚠️ Best Practices

### File Naming
- Use descriptive names for templates
- Keep names list organized
- Backup important templates

### Data Validation
- Check for empty names
- Handle special characters
- Remove duplicate names

### Testing
- Test with a small sample first
- Verify placeholder replacement
- Check output formatting

## 🤝 Contributing

Contributions are welcome! Feel free to:
- 🐛 Report bugs
- 💡 Suggest new features
- 🔧 Submit pull requests
- 📝 Improve documentation
- 🎨 Add new templates

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Lakum Sai Charan**
- GitHub: [@lakumsaicharan](https://github.com/lakumsaicharan)
- Part of the 100 Days of Code Challenge
- Python Automation Learning Journey

## 🙏 Acknowledgments

- Built as part of Python file handling practice
- Inspired by real-world office automation needs
- Great for learning practical Python applications
- Thanks to the Python community

## 💡 Pro Tips

### Time-Saving Benefits
- ⏱️ **Manual**: 5 minutes per letter × 100 people = 8+ hours
- ⚡ **Automated**: Less than 1 second for 100 letters!

### Quality Improvements
- ✅ No typing errors
- ✅ Consistent formatting
- ✅ Professional appearance
- ✅ Easy to update and regenerate

## 🎮 Example Output

**Input Template:**
```
Dear [name],

You are invited to celebrate with us!

Best wishes,
The Team
```

**Generated Letter (for "Alice"):**
```
Dear Alice,

You are invited to celebrate with us!

Best wishes,
The Team
```

---

⭐ **Found this useful? Give it a star!** ⭐

*Automate the boring stuff with Python!* ✉️🚀
