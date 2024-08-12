# Task 2: Use RainbowCrack to Decrypt a Windows LM Password Hash

## Steps:

1. **Generate Rainbow Tables**
   - Use the `rtgen` command to create rainbow tables for alphanumeric passwords.
   - Example command:
     ```
     rtgen lm rainbow_table_path 0  characters 0  1  0  0
     ```

2. **Sort Rainbow Tables**
   - Use the `rtsort` command to sort the generated tables for efficient cracking.
   - Example command:
     ```
     rtsort rainbow_table_path
     ```

3. **Obtain LM Hashes**
   - Extract the LM hashes from the SAM database using tools like `pwdump3`.
   - Example command:
     ```
     pwdump3 system_file_path security_file_path > lm_hashes.txt
     ```

4. **Crack Passwords**
   - Use the `rcrack` command with the sorted rainbow tables and the extracted LM hashes to find the plaintext passwords.
   - Example command:
     ```
     rcrack . -h lm_hashes.txt
     ```

## Note:
Ensure that you have the appropriate permissions and legal authority to perform these actions, as they involve accessing and cracking passwords from a Windows system.
```

