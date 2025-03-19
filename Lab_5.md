# Experiment 5  

## Question  
1. **Implement `ps`, `top`, and `kill` commands with their options.**  
2. **Installing, updating, and removing software using the `apt-get` command.**  

## Description  

In this experiment, we will:  
- Use the `ps`, `top`, and `kill` commands to **monitor and manage processes**.  
- Use `apt-get` to **install, update, and remove software** in Debian-based Linux distributions.  

## Screenshot  

![image](https://github.com/user-attachments/assets/ba923f03-dcdd-49a4-91d1-1c44ebfdc492)
![image](https://github.com/user-attachments/assets/227f3a06-e74f-46a0-af9c-96cf56494f1e)
![image](https://github.com/user-attachments/assets/e42d0ab7-5a7c-4cb7-8bca-ab44db884bf1)


## Commands Used  

### **1️⃣ Process Management Commands**  

```bash
# List all currently running processes
ps aux  

# Display a tree view of running processes
ps -ejH  

# Show processes of a specific user (replace username accordingly)
ps -u username  

# Display real-time system processes with CPU & memory usage
top  

# Show only processes of a specific user in top (replace username)
top -u username  

# Kill a process using its PID (replace <PID> with actual process ID)
kill <PID>  

# Kill all instances of a program by name (e.g., kill all Firefox processes)
killall firefox  

# Kill a process forcefully (SIGKILL)
kill -9 <PID>  

# Update package lists before installing new software
sudo apt-get update  

# Upgrade all installed packages to the latest versions
sudo apt-get upgrade  

# Install a specific software package (replace package_name accordingly)
sudo apt-get install package_name  

# Remove a package but keep its configuration files
sudo apt-get remove package_name  

# Remove a package and its configuration files completely
sudo apt-get purge package_name  

# Auto-remove unnecessary dependencies after package removal
sudo apt-get autoremove  

# Clear local package cache to free up space
sudo apt-get clean  
# Auto-remove unnecessary dependencies after package removal
sudo apt-get autoremove  

# Clear local package cache to free up space
sudo apt-get clean  
