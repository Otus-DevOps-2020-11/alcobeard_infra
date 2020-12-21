# alcobeard_infra
alcobeard Infra repository

# Ssh config to access internal host by alias
Host someinternalhost
        ForwardAgent yes
User appuser
HostName 84.201.179.171
IdentityFile ~/.ssh/id_rsa
