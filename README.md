## Step 1: Architecture Overview

<img width="793" height="716" alt="Screenshot 2026-03-19 203659" src="https://github.com/user-attachments/assets/3234e10c-d50c-4ddd-a4ff-68b5efb62495" />


This diagram shows the hybrid IAM flow:
- Active Directory as the identity source
- Okta as the Identity Provider (IdP)
- SSO Application for authentication

All user authentication flows from AD → Okta → Application.


## Step 2: Create Users in Active Directory

<img width="1919" height="1079" alt="create-test-smith-2" src="https://github.com/user-attachments/assets/fc33d426-0387-4891-a6a0-7f1cf508ac72" />


Created and verified test users to simulate real organizational identities.

### Key Actions:
- Provisioned users for testing IAM workflows
- Verified user visibility within Okta
- Prepared accounts for group-based access and MFA testing

### Skills Demonstrated:
- Identity provisioning
- User lifecycle setup
- Directory synchronization validation


## Step 3: Configure Okta AD Agent

<img width="1044" height="1032" alt="troubleshoot3" src="https://github.com/user-attachments/assets/80a9733b-ae9e-4329-8a64-31ccaaee1c85" />


This was the most challenging part of the lab and required extensive troubleshooting.

### Challenges Faced:
- Initial sync failures between AD and Okta
- Misconfigurations in agent setup and connectivity
- Delays in user/group visibility

### How It Was Resolved:
- Reconfigured AD Agent setup
- Verified network connectivity and permissions
- Re-ran imports and validated synchronization logs

### Why This Matters:
Real-world IAM work is rarely smooth — this demonstrates:
- Problem-solving ability  
- Persistence under failure  
- Understanding of identity system dependencies


## Step 4: Verify Agent Connection

<img width="1018" height="925" alt="agentconfigured4" src="https://github.com/user-attachments/assets/77729cd8-4889-488f-a98e-43cbe88ee21e" />


Verified that the Okta AD Agent was successfully installed and connected.

### Key Actions:
- Confirmed agent health status
- Validated communication between AD and Okta
- Ensured readiness for directory imports


## Step 5: Import Users and Groups into Okta

<img width="1919" height="1079" alt="imported-users-groups5" src="https://github.com/user-attachments/assets/81b2a710-0d70-49c7-8e44-7de2a7d61705" />


Imported users and groups from Active Directory into Okta.

### Key Actions:
- Synced directory objects from AD
- Verified imported users and group structures
- Confirmed identity consistency across systems

### Why This Matters:
This enables:
- Centralized identity management  
- Automated provisioning workflows  
- Scalable access control


## Step 6: Add the SSO Application

<img width="961" height="1025" alt="adding-app6" src="https://github.com/user-attachments/assets/5714f8ad-efc0-43d5-b64e-777eb89c77f6" />


Added an application to Okta to enable Single Sign-On (SSO).

### Key Actions:
- Integrated application into Okta
- Prepared environment for authentication flow
- Configured application settings

### Skills Demonstrated:
- Application onboarding in IAM
- SSO configuration fundamentals

---

## Step 7: Configure Sign-On Settings

<img width="961" height="1028" alt="sign-on7" src="https://github.com/user-attachments/assets/e0f1a885-166e-4d9a-ba37-63d4827244f2" />


Configured authentication behavior for the application.

### Key Actions:
- Defined username format
- Configured credential handling
- Applied secure authentication settings

### Why This Matters:
Proper sign-on configuration ensures:
- Seamless user experience  
- Secure authentication flow  
- Compatibility with enterprise identity standards  

---

## Step 8: Assign the Application to Groups

<img width="1917" height="1033" alt="add-assignments8" src="https://github.com/user-attachments/assets/4503cd55-e685-46e6-8586-5bea5038dc18" />


Assigned the application to organizational groups.

### Key Actions:
- Linked app access to groups (IT, HR, Finance)
- Implemented role-based access control (RBAC)
- Reduced need for manual user assignments

### Why This Matters:
RBAC is critical for:
- Scalability  
- Security  
- Simplified access management  

---

## Step 9: Remove a User from a Group in Active Directory

<img width="787" height="1027" alt="removing-user-from-group9" src="https://github.com/user-attachments/assets/59e1d59a-5920-47a5-b712-f2f2698a7abd" />


Removed a user from a security group in AD.

### Key Actions:
- Simulated access removal scenario
- Updated group membership
- Triggered identity lifecycle change

---

## Step 10: Verify the Access Change in Okta

<img width="1919" height="1079" alt="removed-user-from-okta10" src="https://github.com/user-attachments/assets/4afc5f34-455f-4f8a-81da-525b9ef4156b" />


Validated that changes made in AD propagated to Okta.

### Key Actions:
- Confirmed sync behavior
- Verified removal of access
- Ensured policy enforcement consistency

### Why This Matters:
Demonstrates **identity lifecycle management**:
- Join → Move → Leave processes  
- Automatic access updates  
- Reduced security risk  

---

## Step 11: Create the MFA Policy

<img width="870" height="1027" alt="setting-up-mfa-11" src="https://github.com/user-attachments/assets/da3b5bda-a5c3-4215-90ef-06bdf0f4a37d" />


Created a multi-factor authentication (MFA) policy for all staff groups.

### Key Actions:
- Defined policy scope
- Assigned policy to multiple groups
- Established baseline security requirements

---

## Step 12: Configure the MFA Rule

<img width="884" height="1033" alt="mfa-rule-12" src="https://github.com/user-attachments/assets/e02b36f7-70bd-4b8d-8dee-071f0ef9af1c" />


Configured enforcement rules for MFA.

### Key Actions:
- Required MFA at every sign-in
- Defined session security behavior
- Strengthened authentication controls

### Why This Matters:
MFA significantly reduces:
- Account compromise risk  
- Credential-based attacks  
- Unauthorized access  

---

## Step 13: Configure the Authentication Rule

<img width="876" height="1030" alt="authentication-rule-okta-13" src="https://github.com/user-attachments/assets/1381721b-a625-4d4c-a2e0-5593a8af7f5a" />


Configured authentication flow and allowed factors.

### Key Actions:
- Defined authentication requirements
- Applied strong factor constraints
- Controlled how users verify identity

---

## Step 14: Edit the Authenticator Enrollment Policy

<img width="880" height="1023" alt="edit-authenticator-policy-14" src="https://github.com/user-attachments/assets/ee16669b-e287-4a63-b92f-75c1a9124c63" />

Configured required authenticators for users.

### Key Actions:
- Required Okta Verify (FastPass)
- Required password authentication
- Enforced phishing-resistant authentication methods

### Skills Demonstrated:
- Zero Trust principles  
- Strong authentication enforcement  
- Identity security best practices
