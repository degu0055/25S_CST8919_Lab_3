<!-- 

repo link:
https://github.com/degu0055/25S_CST8919_Lab_3 

-->

# Azure Policy Lab - MapleTech Solutions

## Summary

This lab is about making sure all resources follow company rules in Azure.  
I created 3 custom policies:  
1. Allow resources only in Canada Central region.  
2. Require all resources to have a tag called `ProjectName`.  
3. Block creation of Public IP addresses.  

I put these policies together into one initiative called **MapleTech Secure Foundation**.  
Then I assigned it to a resource group to enforce these rules.

## Explanation of Each Policy

- **Only-CanadaCentral**: Denies resources deployed outside Canada Central.  
- **Require-ProjectName-Tag**: Denies resources that do not have the `ProjectName` tag.  
- **Deny-Public-IP**: Denies creation of any Public IP address resource.

## Test Results

- Deploy VM in Canada Central with tag ✅ Allowed  
  ![VM Deployment Allowed](screenshots/0-vm-allowed.png)

- Deploy VM in East US (not allowed)  
  ![VM Deployment Denied](screenshots/1%20-%20vm.png)

- Deploy Storage Account without ProjectName tag (not allowed)  
  ![Storage Account Denied](screenshots/2%20-%20storageaccount.png)

- Create Public IP address (not allowed)  
  ![Public IP Denied](screenshots/3%20-%20public%20ip%20address.png)

## Challenges and Lessons Learned

- Writing the policy JSON needs careful structure.  
- Testing helped to understand how Azure Policy blocks resources.  
- Tagging is very important for resource organization and compliance.  

---

## Video Demo Link

[Watch demo video here](https://www.youtube.com/watch?v=YOUR_VIDEO_ID)
