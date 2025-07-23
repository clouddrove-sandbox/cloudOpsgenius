# 📘 Ansible Automation - 23 July

## 🎯 Objective

This Ansible project contains hands-on playbooks for managing remote servers using automation. The following tasks are covered:

- Remote server connectivity test
- App installation
- Copying files
- Backing up and modifying files
- Changing permissions and managing files/directories

---

## 📁 Directory Structure

```bash
.
├── app_install.yml           # Install apps (e.g., Nginx) on remote server
├── change_permission.yml     # Manage file/directory permissions
├── copy_files.yml            # Copy files to remote server
├── files_mod.yml             # Modify or backup existing files
├── first_pb.yml              # Initial ping/connection test
└── hosts                     # Inventory file with target remote hosts
```
---



## ⚙️ How to Use

> Make sure Ansible is installed and SSH access is set up to the remote servers.

### 1️⃣ Inventory Setup

Edit the `hosts` file and define your target servers. Example:

```ini
[webservers]
192.168.1.100 ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/id_rsa
```

---

### 2️⃣ Run Playbooks

#### ✅ Test Connection to Remote Server

```bash
ansible-playbook first_pb.yml -i hosts
```

#### 📦 Install Application (e.g., Nginx)

```bash
ansible-playbook app_install.yml -i hosts
```

#### 📁 Copy Files to Remote Server

```bash
ansible-playbook copy_files.yml -i hosts
```

#### 📝 Modify or Backup Existing Files

```bash
ansible-playbook files_mod.yml -i hosts
```

#### 🔐 Change Permissions & Manage Files

```bash
ansible-playbook change_permission.yml -i hosts
```

---

## 🧾 Notes

- Run with `--check` to do a dry-run:
  ```bash
  ansible-playbook app_install.yml -i hosts --check
  ```
- Use `-v`, `-vv`, or `-vvv` for verbose/debug output

---

Copy
Edit
ansible-playbook app_install.yml -i hosts --check
Use -v, -vv, or -vvv for verbose/debug output

