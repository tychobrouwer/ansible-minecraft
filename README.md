Install and configure a Minecraft server
=========

The role will install and configure a Paper Minecraft server for my servers.

Role Variables
--------------

```minecraft_paper_version``` can be set to the Paper version for the server.

```minecraft_paper_build``` can be set to the Paper version for the server.

```minecraft_java_version``` can be set to the Java version required for the selected Paper server.

Example Playbook
----------------

```yaml
    - hosts: servers

      roles:
         - { role: tychobrouwer.minecraft, minecraft_paper_version: 1.20.6, minecraft_paper_build: 145, minecraft_java_version: 21 }
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
