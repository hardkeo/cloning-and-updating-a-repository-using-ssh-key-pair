# how-to-install
How to install some things I'm using.

## Cloning and updating this repository
```bash
# Create a source file
tee git-<git-id> <<-EOF
export GIT_SSH_COMMAND='ssh -i ~/.ssh/<git-private-key> -o IdentitiesOnly=yes'
export GIT_AUTHOR_EMAIL='<git-email-access>'
export GIT_AUTHOR_NAME='<git-id>'
EOF

# Load source file git-<git-id>
source git-<git-id>

# Clone repository
git clone git@github.com:hardkeo/how-to-install.git

# Update repository (after changes)
git push origin main
```