Ansible role: DevkitPro 
=========

An Ansible Role that installs Devkitpro and devkit tools on Debian/Ubuntu/Pop_Os!.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

```
platforms_enabled:
  - gp2x
  # - gp32
  # - gba 
  # - nds
  # - 3ds
  # - gamecube
  # - wii
  # - wiiu
  # - switch
```
Depending on the devkit you'd like to install, add or remove lines containing your desired platforms without the suffix "-dev". 

See [on the official doc](https://devkitpro.org/wiki/devkitPro_pacman#Using_Pacman) which platforms are supported.


Dependencies
------------

None.


Example Playbook
----------------

```
- hosts: all
  vars_files:
    - vars/main.yml
  roles:
    - { role: dag7dev.devkitpro }
```

Inside vars/main.yml:
```
platforms_enabled:
  - gba
  - nds
```


License
-------

MIT / BSD


Author Information
------------------

This role was created in 2023 by Damiano Gualandri, author of [awesome stuff](github.com/dag7dev).