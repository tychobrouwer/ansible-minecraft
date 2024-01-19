Install and configure a Minecraft server
=========

The role will install and configure a Spigot Minecraft server for my servers.

Role Variables
--------------

```minecraft_spigot_version``` can be set to the SpigotMC version for the server.

```minecraft_java_version``` can be set to the Java version required for the selected SpigotMC server.

```minecraft_server_prop``` can be set to the server properties for the server, below the default values are shown.

Example Playbook
----------------

```yaml
    - hosts: servers
      vars:
        minecraft_server_prop:
          enable_rcon: false
          rcon_password: ""
          rcon_port: 25575
          enable_query: false
          query_port: 25565
          server_port: 25565
          level_seed: ""
          enable_command_block: false
          level_name: world
          motd: "A Minecraft Server"
          gamemode: survival
          server_ip: ""
          op_permission_level: 4
          function_permission_level: 2
          pvp: true
          difficulty: hard
          hardcore: false
          level_type: minecraft\:normal
          generate_structures: true
          max_tick_time: 60000
          max_players: 20
          view_distance: 10
          simulation_distance: 10
          player_idle_timeout: 0
          rate_limit: 0
          white_list: false
          enforce_whitelist: false
          allow_flight: false
          allow_nether: true
          spawn_npcs: true
          spawn_animals: true
          spawn_monsters: true
          spawn_protection: 16
          max_world_size: 29999984
          require_resource_pack: false
          resource_pack: ""
          resource_pack_sha1: ""

      roles:
         - { role: tychobrouwer.minecraft, spigot_version: 1.20.4, java_version: 17 }
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
