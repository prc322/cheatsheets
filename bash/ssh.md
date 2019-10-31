# ssh

## create keypair

```bash
$ ssh-keygen -t rsa
```

## set file permissions

```bash
# use 600 to make the files editable
$ chmod 400 id_*
```

## copy public key to remote

```bash
$ ssh-copy-id user@remote
```

## login with key from specfic location

```bash
$ ssh -i /Volumes/keydrive/id_rsa user@remote
```