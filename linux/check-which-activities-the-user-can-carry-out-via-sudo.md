# Check which activities the user can carry out via sudo

`sudo -l` can be used to list all activities a user can carry out via sudo

```
alice@the-machine:~$ sudo -l
Matching Defaults entries for alice on the-machine:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin

User alice may run the following commands on the-machine:
    (ALL : ALL) NOPASSWD: ALL
```

`sudo -l` can be executed via `sudo -u` to check other user priviledges as well.

```
alice@the-machine:~$ sudo -u bob sudo -l
Matching Defaults entries for bob on the-machine:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin

User bob may run the following commands on the-machine:
    (ALL : ALL) NOPASSWD: ALL
```
