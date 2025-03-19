# **Experiment 8: Shell Scripting and Redirection in Linux**  

## **Question**  
1. **Write a shell script to print system information.**  
2. **Write a shell script to perform basic mathematical calculations.**  
3. **Use redirection operators to store the output of commands.**  

## **Description**  
In this experiment, we will:  
- **Write a shell script** to display system information such as OS details, CPU usage, and memory status.  
- **Create a shell script** to perform basic mathematical calculations (addition, subtraction, multiplication, division).  
- **Use redirection operators** (`>`, `>>`) to store command output in files.  

## **Screenshot**  

![image](https://github.com/user-attachments/assets/5e7de07a-d9b5-4337-bd47-ca48955de097)
![image](https://github.com/user-attachments/assets/10deea5b-0d57-4068-b8bc-b4a45e2d83e6)
![image](https://github.com/user-attachments/assets/42bf55cb-8b3e-4b41-9964-c7ebcdbbf993)

## **Commands & Scripts Used**  

### **1️⃣ Shell Script to Print System Information**  
**Create a script file named `sys_info.sh`**  

```bash
#!/bin/bash

echo "===== System Information ====="
echo "Hostname: $(hostname)"
echo "Operating System: $(uname -o)"
echo "Kernel Version: $(uname -r)"
echo "CPU Information: $(lscpu | grep 'Model name')"
echo "Memory Usage: "
free -h

echo "Disk Usage: "
df -h

chmod +x sys_info.sh
./sys_info.sh

** Create a script file named math_calc.sh
#!/bin/bash

echo "Enter first number: "
read num1
echo "Enter second number: "
read num2

echo "Select operation: "
echo "1. Addition"
echo "2. Subtraction"
echo "3. Multiplication"
echo "4. Division"
read choice

case $choice in
    1) result=$((num1 + num2))
       echo "Result: $result" ;;
    2) result=$((num1 - num2))
       echo "Result: $result" ;;
    3) result=$((num1 * num2))
       echo "Result: $result" ;;
    4) if [ $num2 -ne 0 ]; then
           result=$((num1 / num2))
           echo "Result: $result"
       else
           echo "Error: Division by zero!"
       fi ;;
    *) echo "Invalid choice!" ;;
esac

chmod +x math_calc.sh
./math_calc.sh

./sys_info.sh > system_info.txt
cat system_info.txt

./math_calc.sh >> calculations.txt
cat calculations.txt
