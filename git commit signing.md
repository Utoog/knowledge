
Get your gpg key list:
```shell
gpg --list-keys
```

Set up repo for commit signing:
```shell
git config user.signingkey [KEY_ID]
````

Enforce commit signing by default:
```shell
git config commit.gpgsign true
```
