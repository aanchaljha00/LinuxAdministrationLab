# Experiment: User Management in Linux  

## Question  
1. **Create the `operator1` user and confirm that it exists in the system. Set the password for `operator1`.**  
2. **Create additional `operator2` and `operator3` users. Set their passwords as well.**  
3. **Run the `usermod -c` command to update the comments of the `operator1` user account.**  
4. **Remove the `operator3` user from the system.**  

## Description  

In this experiment, we will:  
- **Create user accounts (`operator1`, `operator2`, `operator3`).**  
- **Set passwords for the users.**  
- **Modify user account details using `usermod`.**  
- **Delete a user (`operator3`).**  

## Screenshot  

![image](https://github.com/user-attachments/assets/4179c961-5ff6-47cd-9d8b-0a6e2a79b3c2)

## Commands Used  

```bash
# 1. Create the operator1 user with a home directory
sudo useradd -m -s /bin/bash operator1

# 2. Set a password for operator1
sudo passwd operator1

# 3. Verify if operator1 was created
getent passwd operator1

# 4. Create operator2 and operator3 users with home directories
sudo useradd -m -s /bin/bash operator2
sudo useradd -m -s /bin/bash operator3

# 5. Set passwords for operator2 and operator3
sudo passwd operator2
sudo passwd operator3

# 6. Verify if operator2 and operator3 exist
getent passwd operator2
getent passwd operator3

# 7. Modify operator1 user details (add a comment)
sudo usermod -c "Primary Operator Account" operator1

# 8. Remove operator3 user but keep home directory
sudo userdel operator3

# 9. Remove operator3 user along with their home directory
sudo userdel -r operator3

# 10. Verify if operator3 is deleted
getent passwd operator3
