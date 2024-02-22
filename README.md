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
- Once you've connected to the SSID created, the web gui is available at http://10.3.141.1
- 	PiHole is available at http://10.3.141.1:8080/admin
- If there's 100%+ cpu utilisation, there's a bug with dhcpcd in the raspap container. 

Give it some restarts, that might help? (`docker exec -it raspap bash` then `sudo service dhcpcd restart`)
