# transmission-openvpn-jackett-sonarr-radarr
Docker-compose to run jackett, sonarr and radarr using the same network than transmission-openvpn.  In other words, the transmission-openvpn creates a VPN connection and the other container will run using the same connection.


This docker-compose file is based in:

https://github.com/haugene/docker-transmission-openvpn <br/>
https://github.com/linuxserver/docker-jackett <br/>
https://github.com/linuxserver/docker-sonarr <br/>
https://github.com/linuxserver/docker-radarr <br/>


as folder structure, it uses:

<table>
    <tr>
        <td>/volume1/torrent/transmission</td><td>to save Transmission's configuration</td>
    </tr>
    <tr>
        <td>/volume1/torrent/data</td><td>Transmission's download folder</td>
    </tr>
    <tr>
        <td>/volume1/torrent<td>to save Jackett configuration </td>
    </tr>
    <tr>
        <td>/volume1/torrent/sonarr</td><td>to save Sonarr's configuration</td>
    </tr>
    <tr>
        <td>/volume1/torrent/radarr</td><td>to save Radarr's configuration</td>
    </tr>
    <tr>
        <td>/volume1/movies</td><td>Movies folder</td>
    </tr>
    <tr>
        <td>/volume1/shows</td><td>TV Shows folder</td>
    </tr>
    <tr>
        <td>/volume1/anime</td><td>Anime folder.</td>
    </tr>
</table>

The PGID and PUID should be actived user in the host.  And the folders should have the permission for that user too.

