# 💻 Bash Terminal

This repository contains practical exercises for working with the Linux command-line interface (CLI), managing files, navigating directories, and automating basic operations using Bash.

---

### Task 1: Working with files and directories

```bash
cd ~                                   # Open home directory via terminal
pwd                                    # Show current directory path (identify where you are)
mkdir test1                            # Create a directory named test1 inside current folder
cd test1                               # Go to directory test1
touch file1.txt file2.txt file3.txt    # Create files 1, 2 and 3 inside directory test1
ls                                     # Check directory test1 content
cd ~                                   # Go back to home directory
mkdir test2                            # Create directory test2 inside home directory
rmdir test2                            # Delete directory test2
rm test1/file2.txt                     # Delete file 2 from directory test1
mkdir test3 && touch test3/file4.txt test3/file5.txt # Create directory test3 and add two files into it
rm -rf test3                           # Delete directory test3 (with its contents)
mkdir test4                            # Create directory test4 in home directory
mv test1/file1.txt test1/file3.txt test4/ # Move file1.txt and file3.txt from test1 to test4
echo "line1" >> test4/file1.txt        # Add line 1 to file 1
echo "line2" >> test4/file1.txt        # Add line 2 to file 1
echo "line3" >> test4/file1.txt        # Add line 3 to file 1
cat test4/file1.txt                    # Check content of file 1
echo "line1" >> test4/file3.txt        # Add line 1 to file 3
echo "line2" >> test4/file3.txt        # Add line 2 to file 3
echo "line3" >> test4/file3.txt        # Add line 3 to file 3
cat test4/file1.txt test4/file3.txt    # View contents of two files (1 and 3) at once
nano test4/file1.txt                   # Open text editor to replace all lines in file 1 manually
```
### Task 2: Advanced file operations, text processing, and networking

```bash
cd ~                                   # Open home directory via terminal
mkdir test3                            # Create a directory named test3
# Create files 4, 5, 6 with 4 rows each using a multi-line echo
echo -e "row1\nrow2\nrow3\nrow4" > test3/file4.txt
echo -e "row1\nrow2\nrow3\nrow4" > test3/file5.txt
echo -e "row1\nrow2\nrow3\nrow4" > test3/file6.txt

grep "row2" test3/file5.txt            # Find the string "row2" in file 5
grep -r "row" test3/                   # Find the string "row" inside test3 directory
grep -c "row" test3/file6.txt          # Count lines containing "row" in file 6
find test3/ -name "file5.txt"          # Find file 5 inside test3 directory
find test3/ -name "file5.txt" -delete  # Delete file 5 using find command
echo "test" > test3/file4.txt          # Overwrite file 4 with the word "test"
sed -i 's/test/fail/g' test3/file4.txt # Replace the word "test" with "fail" in file 4
echo "test" >> test3/file4.txt         # Append the word "test" to file 4, keeping existing content

ps aux                                 # View all running processes for all users in the system
kill 1234                              # Kill a non-essential process by its PID (replace 1234 with actual PID)

ping rusau.net                         # Check availability of rusau.net resource
ping -c 5 rusau.net                    # Send exactly 5 packets to rusau.net website

# Fetch information about pets with available status via GET request using curl
curl -X GET "https://swagger.io" -H "accept: application/json"

# Create a new user via POST request using curl with JSON data payload
curl -X POST "https://swagger.io" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{"id":0,"username":"qa_student","firstName":"Ivan","lastName":"Ivanov","email":"qa@test.com","password":"123","phone":"123","userStatus":0}'
```
