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
  vars:
    minecraft_properties_template: templates/server.properties.j2

  roles:
    - role: tychobrouwer.minecraft
    
    - role: tychobrouwer.minecraft
      minecraft_paper_version: 1.20.6
      minecraft_paper_build: 145
      minecraft_java_version: 21
      minecraft_java_deb_key: https://apt.corretto.aws/corretto.key
      minecraft_java_deb_repo: deb https://apt.corretto.aws stable main
      minecraft_java_package: java-21-amazon-corretto-jdk
      minecraft_level_name: world
      minecraft_chunky: true
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
