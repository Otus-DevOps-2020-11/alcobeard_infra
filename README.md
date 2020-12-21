# alcobeard_infra
alcobeard Infra repository

### Lecture 5, homework 3


bastion_IP = 84.201.179.171 \
someinternalhost_IP = 10.129.0.28


> Accessing isolated server with "ssh someinternalhost" style
>
```
Host someinternalhost
    Hostname 84.201.179.171
    Port 22
    User appuser
    IdentityFile ~/.ssh/id_rsa.pub
    RequestTTY force
    ForwardAgent yes
    RemoteCommand ssh appuser@10.129.0.28
```
> Add ssl cert to prevent "untrusted" error

Go to https://sslip.io/ and check default DNS for IP:
```
dig +short 84-201-179-171.sslip.io
```
Go to 84-201-179-171.sslip.io -> Settings -> Let's Encrypt Domain: enter here your default DNS: "84-201-179-171.sslip.io"
