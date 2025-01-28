# EC2 Instance Management and Automation

## Task 1: Create Three EC2 Instances (2 Ubuntu, 1 AWS Linux)

In this task, we use Ansible to automate the creation of three EC2 instances:
- Two Ubuntu instances
- One AWS Linux instance

We used a loop in the Ansible playbook to dynamically create instances based on a given configuration.

### Steps:
- Define the instance types, AMIs, and region in the playbook.
- Use a loop to create the instances.
- Ensure that the correct AMIs are used for Ubuntu and AWS Linux.

---

## Task 2: Set Up Password-less SSH Authentication in All Instances

In this task, we configure password-less SSH authentication on all the EC2 instances created in Task 1.

### Steps:
- Generate an SSH key pair.
- Use the `ssh-copy-id` command to add the public key to each EC2 instance for password-less authentication.
- Test SSH access to ensure that no password is required for login.

---

## Task 3: Automate Shutdown on Ubuntu Instances Only Using a Condition (When Condition)

In this task, we use Ansible to automate the shutdown of only the Ubuntu instances based on the operating system type.

### Steps:
- Gather facts about the instances to identify their OS family.
- Use the `when` condition in the playbook to check if the OS family is `Debian` (which includes Ubuntu).
- Shut down only the instances that are running Ubuntu, ensuring other instances (like AWS Linux) are not affected.

---

## Requirements:
- Ansible
- AWS account and EC2 instances setup
- SSH access to EC2 instances
- Ansible collections: `amazon.aws`

## How to Use:
1. Clone the repository:
   ```bash
   git clone https://github.com/Manishrajwar/Provisioning-Configuration-Management.git
