# Experiment:  

## Question  
Use the `touch` command to create sets of empty practice files to use during this lab.  
- In each set, replace **X** with the numbers **1 through 6**.  
- Create six files with names of the form:  
  - `songX.mp3`  
  - `snapX.jpg`  
  - `filmX.avi`  
- Create three subdirectories for organizing your files, and name the subdirectories:  
  - `friends`  
  - `family`  
  - `work`  
- Use a **single command** to create all three subdirectories at the same time.  

## Description  

In this experiment, we use:  
1. **File Creation**  
   - The `touch` command to create **six** sets of empty files.  
   - We replace **X** with numbers **1 to 6** in file names.  
2. **Directory Creation**  
   - The `mkdir` command to create multiple directories in **one command**.  

## Screenshot  
![image](https://github.com/user-attachments/assets/b2b368c3-a6d9-4719-b13a-9462319bb58c)


## Commands Used  

```bash
# 1. Navigate to the Desktop (or preferred location)
cd ~/Desktop

# 2. Create a directory for organizing the files
mkdir practice_lab && cd practice_lab

# 3. Use the touch command with brace expansion to create multiple empty files
touch song{1..6}.mp3 snap{1..6}.jpg film{1..6}.avi

# 4. Create all three subdirectories at the same time
mkdir friends family work

# 5. Verify the created files and directories
ls -l
