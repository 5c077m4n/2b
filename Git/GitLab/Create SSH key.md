- Generate SSH keypair (can use an empty passphrase)
```shell
ssh-keygen -t ed25519 -C "<comment>" # ED25519 is the most secure aglorithem (as of now)
eval $(ssh-agent -s)
ssh-add <new private key path>
```

- Update the `$HOME/.ssh/config` file:
```ssh-config
# GitLab.com
Host gitlab.com
	  PreferredAuthentications publickey
	  IdentityFile ~/.ssh/gitlab_com_rsa

# Private GitLab instance
Host gitlab.company.com
	  PreferredAuthentications publickey
	  IdentityFile ~/.ssh/example_com_rsa
```
  
- Add public key to gitlab.com SSH keys page (in settings)