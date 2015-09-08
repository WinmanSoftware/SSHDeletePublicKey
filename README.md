# SSSDeletePublicKey
Interactively list users and their public keys that the SSH server accepts for Public Key Authentication.

## Working
*SSHDeletePublicKey* will list the users currently having keys for PKA on the server. Once a specific user is chosen, it will then list the public keys that the server will accept for them. You can shoose which key you want to delete.

Upon confirmation, the script will then modify file permissions of `~/.ssh/authorized_keys`, delete the specific public key. and then revert the file permissions back.

## Usage
```bash
$ SSHDeletePublicKey [username]
```
`SSHDeletePublicKey` accepts one optional parameter.
*  `username` specifies the user whose public keys in `~/.ssh/authorized_keys` will be listed.
