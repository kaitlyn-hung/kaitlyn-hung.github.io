# Python File Processing Script

### Purpose
Script to **read an existing allow list, remove unauthorized IP addresses, and rewrite the updated list back to the file** using Python. This demonstrates basic file processing and automation skills that are useful for managing security-related data.

---
### Automating Authorized IP Updates
```python
# Specify the file that stores the current list of approved addresses
import_file = "allowed_hosts.txt"

# File with addresses to remove
remove_file = "removed_hosts.txt"

# Open the file and read its contents into memory, split simultaneously
with open(import_file, "r") as f: 
    ip_addresses = f.read().split()

# Read the addresses to remove and split simultaneously
with open(remove_file, "r") as f:
    remove_list = f.read().split()

# Loop through each address that should be taken off the list
for address in remove_list:

  # Check if the banned address exists in the current list
  if address in ip_addresses:

      # Remove the banned address from the list
      ip_addresses.remove(address)

# Convert the updated list back into a newline-separated string for writing
updated_ip_addresses = "\n".join(ip_addresses)

# Write the revised data back into the original file
with open(import_file, "w") as file: 
  file.write(updated_ip_addresses)
```


### How It Works

