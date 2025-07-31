# Azure Policy Lab – MapleTech Secure Foundation

## Summary
In this lab, we enforced three custom Azure Policies—region lockdown, mandatory tagging, and blocking public IPs—grouped in the “MapleTech Secure Foundation” initiative and assigned to our `rg-policy-lab` resource group.

## Policy Definitions
- **Only-CanadaCentral**: Denies resources outside Canada Central.  
- **Require-ProjectName-Tag**: Ensures every resource has a `ProjectName` tag.  
- **Deny-Public-IP**: Prevents creation of public IP addresses.

## Test Results
1. **VM in East US**: Denied.  
2. **Storage w/o tag**: Denied.  
3. **Public IP**: Denied.  
4. **VM in Canada Central with tag**: Allowed.

## Challenges & Lessons
- Verifying correct policy JSON syntax (watch out for braces!).  
- Understanding Azure’s “effect”: `deny` vs. `audit`.

## Demo Video
[Watch the 10-minute policy demo](https://youtu.be/uVqU23mzkys)