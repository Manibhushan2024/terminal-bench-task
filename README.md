# terminal-bench-task
# 🗂️ File Operations Basic Task

A comprehensive terminal benchmark task demonstrating Bash file operations with complete testing and Docker containerization.

## 📋 Task Description

**Create a Bash script that performs the following file operations:**
1. Create a new directory called `test_data`
2. Create a text file named `sample.txt` with content "Hello World"
3. Make a copy of `sample.txt` called `backup.txt`
4. List all files in the `test_data` directory
5. Display contents of both files to verify they are identical

## 🚀 Quick Start

```bash
# Make solution executable and run
chmod +x solution.sh
./solution.sh

# Expected output:
# backup.txt  sample.txt
# Contents of sample.txt:
# Hello World
# Contents of backup.txt:
# Hello World


📁 Project Structure
file-operations-basic/
├── 📄 task.yaml              # Task configuration & instructions
├── 🐚 solution.sh            # Complete Bash solution
├── 🐳 Dockerfile             # Ubuntu container setup
├── 🐳 docker-compose.yaml    # Docker compose configuration
├── 🧪 run-tests.sh           # Test execution script
└── 📂 tests/
    └── 🐍 test_outputs.py    # Comprehensive test cases

🛠️ Technologies Used
Technology	Purpose
Bash Scripting	Core task implementation
Python pytest	Test framework
Docker	Containerization
Ubuntu Linux	Execution environment
🧪 Test Suite Coverage
Test Case	Description	Status
test_test_data_directory_exists	Verifies directory creation	✅
test_sample_file_exists	Checks sample.txt existence	✅
test_backup_file_exists	Checks backup.txt existence	✅
test_files_have_correct_content	Validates file contents	✅
test_directory_listing	Verifies directory listing	✅
🏃‍♂️ Execution Methods
Manual Execution
./solution.sh

Docker Testing
bash
# Test with oracle agent (should pass)
uv run tb run --agent oracle --task-id file-operations-basic

# Test with nop agent (should fail)
uv run tb run --agent nop --task-id file-operations-basic

# Interactive debugging
uv run tb tasks interact -t file-operations-basic
📊 Task Metadata
📊 Difficulty: Easy

📂 Category: File Operations

🏷️ Tags: files, linux, bash, basic, file-operations

⏱️ Timeout: 300 seconds

👨‍💻 Author: Manibhushan Kumar

📧 Email: manibhushank437@gmail.com

🔧 Solution Script (solution.sh)
bash
#!/bin/bash
# Create test directory
mkdir test_data

# Create sample file with content
echo "Hello World" > test_data/sample.txt

# Create backup copy
cp test_data/sample.txt test_data/backup.txt

# List files
ls test_data/

# Verify contents
echo "Contents of sample.txt:"
cat test_data/sample.txt

echo "Contents of backup.txt:"
cat test_data/backup.txt
🧪 Sample Test Case (test_outputs.py)
python
def test_files_have_correct_content():
    """Test that both files have the correct content"""
    sample_path = Path("/app/test_data/sample.txt")
    backup_path = Path("/app/test_data/backup.txt")
    
    sample_content = sample_path.read_text().strip()
    backup_content = backup_path.read_text().strip()
    
    assert sample_content == "Hello World", f"Expected 'Hello World', got '{sample_content}'"
    assert backup_content == "Hello World", f"Expected 'Hello World', got '{backup_content}'"
    assert sample_content == backup_content, "File contents should be identical"
🐳 Docker Configuration
Base Image: Ubuntu 24.04
Includes: bash, coreutils, tmux, asciinema
Workdir: /app

🎯 Skills Demonstrated
✅ Bash Scripting - File system operations

✅ Test-Driven Development - Comprehensive pytest suite

✅ Docker Containerization - Environment setup

✅ Linux System Administration - File operations

✅ Automated Testing - Validation and verification

✅ Documentation - Clear instructions and metadata

📝 Assessment Compliance
Requirement	Status
Self-contained instructions	✅
Deterministic solution	✅
Comprehensive test suite	✅
Docker containerization	✅
Clear documentation	✅
👨‍💻 Author Information
Manibhushan Kumar
📧 Email: manibhushank437@gmail.com
🐙 GitHub: Manibhushan2024
🔗 LinkedIn: Manibhushan Kumar

📜 License
This project is created as part of the AfterQuery Software Engineer assessment. All rights reserved.

⭐ If you find this useful, please star the repository!

"The superior man understands what is right; the inferior man understands what will sell." - Confucius

text

## **To use this:**

1. **Create README.md file:**
```bash
nano README.md
