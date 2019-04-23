# transmission-openvpn-jackett-sonarr-radarr
Docker-compose to run jackett, sonarr and radarr using the same network than transmission-openvpn.  In other words, the transmission-openvpn creates a VPN connection and the other container will run using the same connection.


This docker-compose file is based in:

https://github.com/haugene/docker-transmission-openvpn
https://github.com/linuxserver/docker-jackett
https://github.com/linuxserver/docker-sonarr
https://github.com/linuxserver/docker-radarr


as folder structure, it uses:

<table>
    <tr>
        <td>Foo</td>
    </tr>
</table>

|- /volume1/torrent/transmission    | to save Transmission's configuration  |
|- /volume1/torrent/data            | Transmission's download folder        |
|- /volume1/torrent/jackett         | to save Jackett configuration         |
|- /volume1/torrent/sonarr          | to save Sonarr's configuration        |
|- /volume1/torrent/radarr          | to save Radarr's configuration        |
|- /volume1/movies:/movies          | Movies folder                         |
|- /volume1/shows:/tv               | TV Shows folder                       |
|- /volume1/anime:/anime            | Anime folder.                         |


The PGID and PUID should be actived user in the host.

