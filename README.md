# Home Assistant Add-on: RustDesk-Server

[![GitHub Release][releases-shield]][releases]
[![License][license-shield]](LICENSE)

![Supports aarch64 Architecture][aarch64-shield]

[RustDesk-Server][rustdesk-server] permet de partager des fichiers avec d'autres de manière
simple.

[![Open your Home Assistant instance and show the add add-on repository dialog
with a specific repository URL pre-filled.][add-repo-shield]][add-repo]
[![Open your Home Assistant instance and show the dashboard of a Supervisor add-on.][add-addon-shield]][add-addon]

## About

Cet add-on vous permet d'auto-hébergez votre propre serveur RustDesk
sur votre HomeAssistant sur RaspBerry Pi 4.
Si vous utilisez RustDesk, vous devriez avoir votre propre server RustDesk.
Les serveurs publics Rustdesk sont destinés à des fins de test et de recherche
et ne sont pas équipés pour gérer de grandes quantités de trafic.
Cela signifie que le temps nécessaire pour établir une connexion
via les serveurs publics peut varier considérablement et parfois même échouer
si le serveur est surchargé.
De plus, si la perforation échoue un jour et que la connexion est acheminée
via le serveur relais public... certains jours elle peut être
extrêmement rapide... d'autres moins.

## Support

Je ne suis pas dévellopeur, n'ai aucune formation de code, je suis simplement
autodidact.
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

[add-addon]: https://my.home-assistant.io/redirect/supervisor_addon/?addon=c751e21a_rustdesk-server
[add-addon-shield]: https://my.home-assistant.io/badges/supervisor_addon.svg
[add-repo]: https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A//github.com/casse-boubou/hassio-addons
[add-repo-shield]: https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg
[releases]: https://github.com/casse-boubou/addon-rustdesk-server/releases
[releases-shield]: https://img.shields.io/github/v/release/casse-boubou/addon-rustdesk-server
[license-shield]: https://img.shields.io/github/license/casse-boubou/addon-rustdesk-server
[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[rustdesk-server]: https://github.com/rustdesk/rustdesk-server
[discord-ha]: https://discord.gg/c5DvZ4e
[forum]: https://community.home-assistant.io
[hacf]: https://forum.hacf.fr/
[Frosh]: https://github.com/casse-boubou
