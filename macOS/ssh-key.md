# SSH Key Management Guide

## Creation of New SSH Key
```bash
ssh-keygen -t rsa
```
This command generates a new RSA type SSH key. The -t rsa flag specifies the key type as RSA. This process involves creating a public and private key pair that can be used for secure communication.

## Configuration to Use SSH Key with Certain Hostname
To use the SSH key with a specific hostname, it's necessary to configure the SSH client. This is typically achieved through the config file located in the `.ssh` directory. 

```bash
Host <hostname>
     HostName <hostname>
     IdentityFile ~/.ssh/id_name
```

- Host: Specifies the hostname for which the following configurations apply.

- HostName: Specifies the actual hostname.

- IdentityFile: Specifies the path to the private key associated with the given hostname.

This configuration allows the system to automatically detect and use the specified SSH key when interacting with the specified hostname.

# Saving SSH Key’s Passphrase in the Apple Keychain
To avoid entering the passphrase repeatedly, it's possible to save it in the Apple Keychain. This involves appending a configuration to the desired hostname in the config file:

```bash
Host github.com
     AddKeysToAgent yes
     UseKeychain yes
     IdentityFile ~/.ssh/id_name
```

- AddKeysToAgent: Enables adding the private key to the SSH agent.

- UseKeychain: Specifies the use of the Apple Keychain to store the passphrase.

This configuration ensures that the passphrase is asked only once, and subsequently, it is saved in the keychain.