# Home Assistant Add-on: RustDesk-server

## About

Cet add-on vous permettra d'auto-hébergez votre propre serveur [RustDesk][rustdesk] sur votre
HomeAssistant sur RaspBerry Pi 4.

Si vous utilisez RustDesk, vous devriez avoir votre propre [server RustDesk][serveur_rustdesk].\
Les serveurs publics Rustdesk sont destinés à des fins de test et de recherche et ne sont pas équipés pour gérer de grandes quantités de trafic.\
Cela signifie que le temps nécessaire pour établir une connexion via les serveurs publics peut varier considérablement et parfois même échouer si le serveur est surchargé.\
De plus, si la perforation échoue un jour et que la connexion est acheminée via le serveur relais public... certains jours elle peut être extrêmement rapide... d'autres moins.

##### _This add-on will allow you to self-host your own [RustDesk][rustdesk] server on your HomeAssistant on RaspBerry Pi 4. If you are using RustDesk you should have your own [RustDesk Server][serveur_rustdesk]. The public rustdesk servers are meant for testing and research purposes and are not equipped to handle large amounts of traffic. This means that the amount of time it takes to establish a connection through the public servers can vary drastically and sometimes even fail if the server is overloaded. Also, if hole punching ever does fail, and the connection is routed through the public Relay Server.... some days it might be blazing fast... others not so much._

## Installation

D'habord ajoutez le repertoire à l'add-on store de HomeAssistant (`https://github.com/casse-boubou/hassio-addons`):

[![Open your Home Assistant instance and show the add add-on repository dialog
with a specific repository URL pre-filled.][add-repo-shield]][add-repo]

Ensuite recherchez RustDesk-server dans le store et cliquez sur installer:

[![Open your Home Assistant instance and show the dashboard of a Supervisor add-on.][add-addon-shield]][add-addon]

## Configuration

Example add-on configuration:

```yaml
private_key: >-
  pmuglkSVWTD3kAw+H9i1WlWWgMFcvkCimlh5W6Ex7/JuHLWRYYIqOUTljEqo9Aea2DI9BQayTCAN89Y4dI8OIw==
public_key: bhy1kWGCKjlE5YutbPQHmtgyPQUGsklWDfPWOHSPDiM=
relay: mondomaine.duckdns.org
```

**Note**: _Ceci n'est qu'un exemple, ne le copier-coller pas ! Crée le votre!_

### Option: `private_key` (optional)

Partie privée de la paire de clés. Si défini, force l'utilisation d'une clé spécifique, s'il est défini sur "\_", force l'utilisation de n'importe quelle clé.

##### _Private part of the key pair. If set force the use of a specific key, if set to "\_" force the use of any key_

### Option: `public_key` (optional)

Partie public de la paire de clés. Si défini, force l'utilisation d'une clé spécifique, s'il est défini sur "\_", force l'utilisation de n'importe quelle clé.

##### _Public part of the key pair. If set force the use of a specific key, if set to "\_" force the use of any key_

### Option: `relay` (optional)

Ce paramètre est l'adresse IP (ou le nom DNS) du serveur exécutant hbbr (généralement ce conteneur). Le paramètre facultatif `port` doit être utilisé si vous utilisez un port différent de 21117 pour hbbr. `e.g rustdesk.example.com:21117`

##### _This parameter is the IP address (or dns name) of the server running hbbr (usualy this container). The optional `port` parameter has to be used if you use a port different than 21117 for hbbr. `e.g rustdesk.example.com:21117`_

## Changelog & Releases

Vous pouvez consulter le changelog [GitHub ici][releases].

## Support

Je ne suis pas dévellopeur, n'ai aucune formation de code, je suis simplement autodidact.
Si vous avez une question concernant HA et ses add-ons vous pouvez consulter:

- [Le Forum communautaire francophone][hacf] de HomeAssistant
- [Le Forum communautaire anglophone][forum] de HomeAssistant.
- [Le serveur Discord][discord-ha] de HomeAssistant.

## License

MIT License

Copyright (c) 2025 [Frosh][Frosh]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[add-addon]: https://my.home-assistant.io/redirect/supervisor_addon/?addon=c751e21a_monerod
[add-addon-shield]: https://my.home-assistant.io/badges/supervisor_addon.svg
[add-repo]: https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fcasse-boubou%2Fhassio-addons
[add-repo-shield]: https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg
[discord-ha]: https://discord.gg/c5DvZ4e
[forum]: https://community.home-assistant.io
[hacf]: https://forum.hacf.fr/
[Frosh]: https://github.com/casse-boubou
[releases]: https://github.com/casse-boubou/addon-rustdesk-server/releases
[rustdesk]: https://rustdesk.com/
[serveur_rustdesk]: https://github.com/rustdesk/rustdesk-server
