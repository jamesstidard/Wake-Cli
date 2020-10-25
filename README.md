# Wake
Wake brings together your ssh config and WakeOnLan together,
so you can use the same aliases you use to ssh to your machines,
to wake them up.

Just as you `ssh mymachine` you can `wake mymachine`.

To use you must add a `MACAddress` entry to your hosts in your `~/.ssh/config`.
So you don't break things, you should add `MACAddress` to the `IgnoreUnknown`.

Example:

```
Host *
 IgnoreUnknown MACAddress
 IdentityFile ~/.ssh/id_rsa

Host mymachine
 Hostname 10.0.0.100
 User myuser
```
