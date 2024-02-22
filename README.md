# RasPiRate

Everything you need to turn a raspberry pi into a self-hosted router, with a recursive ad-blocking DNS!
The `docker-compose.yaml` file spins up and connects:
- [raspAp](https://github.com/RaspAP/raspap-docker)
- [pihole](https://github.com/pi-hole/docker-pi-hole)
- [unbound](https://github.com/MatthewVance/unbound-docker-rpi)
- [watchtower](https://github.com/containrrr/watchtower)

The `.env` file contains most of the configuration that should be needed - values should be self-explantory

### Notes

- Run `docker compose up -d` (not `docker-compose`!)
- Docker will look for volumes - you may need to create them
