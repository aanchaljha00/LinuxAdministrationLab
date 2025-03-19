Question:7
Implement the chown command and explore its options.
Implement the chmod command and explore its options.

Description:
In this experiment, we will:
Change ownership of files and directories using chown.
Modify file permissions using chmod.
Explore different options for both commands.

Screenshot: 
![image](https://github.com/user-attachments/assets/558dae4a-48b9-4949-a4fa-8bf8d3627d83)
![image](https://github.com/user-attachments/assets/beb01e5f-6415-42ae-83dd-7926627986b0)

Commands Used: 
# 1. Create a sample file
touch sample_file.txt

# 2. Change the owner of the file to a specific user
sudo chown username sample_file.txt

# 3. Change both the owner and group of the file
sudo chown username:groupname sample_file.txt

# 4. Change ownership recursively for all files in a directory
sudo chown -R username:groupname /path/to/directory

# 5. Verify the ownership change
ls -l sample_file.txt

# 6. Modify file permissions using symbolic mode
chmod u+rwx sample_file.txt  # Add read, write, and execute for the owner
chmod g-w sample_file.txt    # Remove write permission for the group
chmod o-r sample_file.txt    # Remove read permission for others

# 7. Modify file permissions using octal mode
chmod 755 sample_file.txt

# Explanation of 755 permissions:
# 7 (Owner)   → Read (4) + Write (2) + Execute (1) = 7
# 5 (Group)   → Read (4) + Execute (1) = 5
# 5 (Others)  → Read (4) + Execute (1) = 5

# 8. Change permissions recursively for a directory
chmod -R 700 /path/to/directory

# 9. Verify permission changes
ls -l sample_file.txt
