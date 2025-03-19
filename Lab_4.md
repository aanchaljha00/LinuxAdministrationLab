# Experiment 4:  

## Question  
1. **Create the `/home/consultants` directory.**  
2. **Add write permission to the consultants group** using the symbolic method.  
3. **Forbid others from accessing files** in `/home/consultants` using the octal method.  
4. **Change the default `umask` for the `operator1` user** so that users not in their group cannot access their files.  
5. **Confirm that the `umask` is changed.**  

## Description  

In this experiment, we will:  
- **Create a directory** for consultants.  
- **Modify permissions** using both **symbolic** and **octal** methods.  
- **Change the default `umask`** for a user and verify the change.  

## Screenshot  

![image](https://github.com/user-attachments/assets/cf097d66-b223-4d9f-b9ee-8c76a0f5fb42)

## Commands Used  

```bash
# 1. Create the /home/consultants directory
sudo mkdir /home/consultants

# 2. Add write permission to the consultants group (symbolic method)
sudo chmod g+w /home/consultants

# 3. Forbid others from accessing files in /home/consultants (octal method)
sudo chmod 770 /home/consultants

# Explanation of 770 permission:
# 7 (Owner)   → Read (4) + Write (2) + Execute (1) = 7
# 7 (Group)   → Read (4) + Write (2) + Execute (1) = 7
# 0 (Others)  → No permissions = 0

# 4. Switch to operator1 user (if not already)
su - operator1

# 5. Change the default umask for operator1 to forbid access for others
echo "umask 007" >> ~/.bashrc

# Explanation of umask 007:
# 0 (Owner)  → No restrictions (default full permissions)
# 0 (Group)  → No restrictions (default full permissions)
# 7 (Others) → No permissions (prohibited access)

# 6. Apply the new umask settings
source ~/.bashrc

# 7. Confirm the umask is changed
umasksu - operator1
