# Experiment:  

## Question  
View the **gedit** man page.  
Use the `man -k ext4` command to find the command to tune **ext4** file-system parameters.  
Brace expansion is used to generate discretionary strings of characters. Braces contain a **comma-separated list** of strings, or a **sequence expression**. The result includes the text that precedes or follows the brace definition.  

## Description  

In this experiment, we explore essential Linux commands:  
1. **Viewing the gedit Man Page & Finding ext4 File-System Tuning Commands**  
   - The `man` command is used to view the **manual page** for `gedit`.  
   - The `man -k ext4` command searches for **ext4-related** tuning commands.  
   - The `tune2fs` command is used to **modify ext4 file system parameters**.  

2. **Using Brace Expansion**  
   - Brace expansion simplifies command execution by **generating multiple strings** in a single command.  
   - It supports **comma-separated lists** and **sequences**.  

## Screenshot  

![image](https://github.com/user-attachments/assets/acd7c936-7637-439b-9767-af589cc6062c)
 
## Commands Used  

```bash
# 1. View the gedit manual page
man gedit

# 2. Find commands related to the ext4 file system
man -k ext4

# 3. View the man page for the ext4 tuning command
man tune2fs

# 4. Generate a list of files with different names using brace expansion
echo file_{a,b,c}.txt
# Output: file_a.txt file_b.txt file_c.txt

# 5. Generate a sequence of numbers
echo num_{1..5}
# Output: num_1 num_2 num_3 num_4 num_5

# 6. Generate a list with text before and after
echo report_{jan,feb,mar}_2025.pdf
# Output: report_jan_2025.pdf report_feb_2025.pdf report_mar_2025.pdf

# 7. Create multiple directories using brace expansion
mkdir project_{alpha,beta,gamma}
# Creates directories: project_alpha, project_beta, project_gamma

# 8. Create multiple files using brace expansion
touch log_{1..3}.txt
# Creates: log_1.txt log_2.txt log_3.txt

# 9. Generate a range of numbers with step size
echo seq_{1..10..2}
# Output: seq_1 seq_3 seq_5 seq_7 seq_9

# 10. Create nested directories with brace expansion
mkdir -p parent/{child1,child2,child3}
# Creates directories: parent/child1, parent/child2, parent/child3
