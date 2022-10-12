# Cloning and updating a repository using ssh key pair
How to clone (if private) and/or update reposytory using ssh key pair authentication.

## On CLI:
```bash
# Create a source file
tee ./git-<git-id>-source <<-EOF
  export GIT_SSH_COMMAND='ssh -i ~/.ssh/<git-private-key> -o IdentitiesOnly=yes'
  export GIT_AUTHOR_EMAIL='<git-email-access>'
  export GIT_AUTHOR_NAME='<git-id>'
EOF

# Load source file git-<git-id>-source
source git-<git-id>-source

# Clone repository
git clone git@github.com:hardkeo/how-to-install.git

# Update repository (after changes)
git push origin main
```