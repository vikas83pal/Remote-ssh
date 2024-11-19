# Steps to add ssh key to your github account 
# Generate a New SSH Key
1. Run the following command, replacing your email:
```
ssh-keygen -t ed25519 -C "vikas83pal@gmail.com"

```

- If ed25519 is not supported, use:
```
ssh-keygen -t rsa -b 4096 -C "vikas83pal@gmail.com"

```

2. You’ll be prompted to save the key. Press Enter to accept the default location:
```

Enter file in which to save the key (/Users/you/.ssh/id_ed25519):

```

3. Set a passphrase for extra security (or leave it blank for no passphrase).

# Add the SSH Key to the SSH Agent

- Start the SSH agent:
```
eval "$(ssh-agent -s)"

```

- Add your private key to the agent:

```

ssh-add ~/.ssh/id_ed25519

```

# Add the SSH Key to Your Git Hosting Service

# GitHub:
Copy your public key to the clipboard:
```

cat ~/.ssh/id_ed25519.pub

```
Copy the entire output.

- Go to GitHub SSH Keys Settings.

- Click New SSH Key, add a title (e.g., "My Laptop"), and paste your key.

- Click Add SSH Key.

# GitLab:
- Go to GitLab SSH Keys Settings.

- Paste the public key and give it a title.

- Click Add Key.
