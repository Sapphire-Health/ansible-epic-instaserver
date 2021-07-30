# ansible-ad-join

## Install Dependencies
```
ansible-galaxy collection install -r collections/requirements.yml
```
or
```
ansible-galaxy collection install ogratwicklcs.realmd_ipa_ad
```

## Run playbook
```
ansible-playbook -i hosts.yml -e @vars.yml main.yml
```

## Example YAML
hosts.yml
```
---
  all:
    hosts:
      test-server-name:
        ansible_host: 192.168.1.100
```

vars.yml
```
match_host: test-server-name
ADDomain: yourdomain.org
ADJoinUsername: "YOURDOMAIN\\youradminusername"
ADJoinPassword: "youradminpassword"
```