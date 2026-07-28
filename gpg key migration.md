
```shell
# Export public key
gpg --export -a <key-ID> > gpg-pub.asc

# Export private key
gpg --export-secret-keys -a <key-ID> > gpg-sec.asc
```

```shell
# Import public key
gpg --import gpg-pub.asc

# Import public key
gpg --import gpg-sec.asc
```
