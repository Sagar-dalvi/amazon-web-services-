IAM
IAM :- IAM stands for Identity Access Management 
o	IAM allows you to manage users and their level of access to the aws console.
o	It is used to set users, permissions and roles. It allows you to grant access to the different parts of the aws platform.
o	With IAM, Organizations can centrally manage users, security credentials such as access keys, 
and permissions that control which AWS resources users can access.


---------------------------------------------------------------------------------------------------------------------------------------------

IAM (Identity and Access Management) in AWS is a service that helps you securely control access to AWS services and resources.
It allows you to manage users, groups, and permissions to ensure that only authorized users can perform specific actions.
Here’s a simplified overview and a hands-on guide to get you started:

### Overview

1. **Users**: Individuals who need access to AWS services. Each user has a unique name and credentials.
2. **Groups**: Collections of users that can be managed together. Permissions applied to a group are inherited by all its users.
3. **Roles**: Instead of assigning permissions to users directly, you can assign permissions to roles and then let users or AWS services assume those roles.
4. **Policies**: Documents that define permissions. Policies are attached to users, groups, or roles to grant permissions.

### Key Concepts

- **Authentication**: Verifying the identity of a user or service.
- **Authorization**: Granting or denying permissions to resources.
- **Temporary Credentials**: Short-term access permissions often used for applications or services.

### Hands-On Guide

#### Step 1: Create a User

1. **Navigate to IAM Console**:
   - Sign in to the AWS Management Console and open the IAM console at
[https://console.aws.amazon.com/iam/](https://console.aws.amazon.com/iam/).

2. **Add User**:
   - In the IAM console, click on **Users** on the left sidebar.
   - Click the **Add user** button.
   - Enter a username.
   - Select the type of access: **Programmatic access** (for CLI/SDK access) or **AWS Management Console access**.
   - Set a password for console access if selected.

3. **Set Permissions**:
   - Choose how to set permissions for the user. You can add the user to a group,
     copy permissions from another user, or attach policies directly.

4. **Review and Create**:
   - Review the settings and click **Create user**.
   - Download the CSV file containing the user's access key ID and secret access key for programmatic access.

#### Step 2: Create a Group and Attach Policies

1. **Create a Group**:
   - In the IAM console, click on **Groups**.
   - Click the **Create New Group** button.
   - Enter a group name and click **Next Step**.

2. **Attach Policies to the Group**:
   - Select policies to attach to the group. For example, you can attach the **AmazonS3FullAccess** policy to grant full access to S3.
   - Click **Next Step**, review, and then click **Create Group**.

3. **Add Users to the Group**:
   - Go back to the **Users** section.
   - Select the user you created earlier.
   - Click on the **Add user to group** button.
   - Select the group and click **Add to group**.

#### Step 3: Create a Role

1. **Create a Role**:
   - In the IAM console, click on **Roles**.
   - Click the **Create role** button.
   - Select the type of trusted entity. For example, choose **AWS service** to allow an AWS service to assume the role.
   - Select the service that will use the role, such as **EC2**, and click **Next**.

2. **Attach Policies to the Role**:
   - Select the policies to attach to the role. For example, you can attach the **AmazonEC2FullAccess** policy.
   - Click **Next**, review, and then click **Create role**.

3. **Assign the Role**:
   - Assign the role to an AWS service or allow users to assume the role via the console or API.

### Summary

IAM in AWS helps manage access by organizing users, groups, and roles with specific policies
. This structure ensures that access is granted on a need-to-know basis, improving security and control over AWS resources.
