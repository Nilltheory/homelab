# SSH

## Purpose

SSH (Secure Shell) allows secure remote access to another computer over a network.

It is commonly used by system administrators to manage servers without needing physical access.

---

## What SSH Provides

SSH allows:

- Remote terminal access
- Secure command execution
- File transfers
- System administration

All communication is encrypted.

---

## Basic Concept

Instead of sitting in front of the server, a user can connect remotely:

```bash
ssh username@192.168.x.x
```

Example:

```bash
ssh kanishk@192.168.x.x
```

After authentication, commands can be executed as if sitting directly at the server.

---

## Why It Is Useful

For a homelab, SSH allows:

- Managing the server remotely
- Updating software
- Checking logs
- Configuring services
- Running administrative commands

without needing a monitor or keyboard attached.

---

## Authentication Methods

### Password Authentication

The user enters a password after connecting.

Advantages:
- Simple

Disadvantages:
- Less secure

---

### Public Key Authentication

Uses:

- Private key
- Public key

The public key is stored on the server.

The private key remains with the user.

Advantages:
- More secure
- Resistant to password guessing attacks

---

## Security Considerations

Recommended:

- Use strong passwords
- Disable root login when possible
- Use SSH keys
- Keep software updated

Avoid:

- Exposing SSH to the internet without understanding the risks
- Using weak passwords

---

## Commands Learned

Connect to a server:

```bash
ssh username@ip-address
```

Copy a file to a server:

```bash
scp file.txt username@ip-address:/home/user
```

Check SSH service status:

```bash
systemctl status ssh
```

Restart SSH:

```bash
sudo systemctl restart ssh
```

---

## Future Learning Goals

- SSH key authentication
- SSH configuration files
- Port forwarding
- Tunneling
- Remote administration best practices

---

## Key Takeaways

- SSH is one of the most important tools in Linux administration.
- It provides secure remote access through encryption.
- Most server management tasks can be performed through SSH.
- Learning SSH is essential for networking, system administration, and cybersecurity.