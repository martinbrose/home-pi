# Home Pi

**A Raspberry Pi config for home automation with Home Assistant**

## Features

**Home Assistant**: Installs the Home Assistant Docker configuration so you can manage smart devices across your home network. Use Home Assistant to automate your home!<br>
Supports the install of either the normal Home Assistant Core or the powerful Home Assistant Supervisor (formerly referred to as Hassio / Hass.io). The later is only recommended for experienced users.

 ![Home Assistant on the Home Pi](/images/home-assistant.png)

**AirConnect**: Installs the AirConnect Docker configuration so you can send audio to UPnP/Sonos/Chromecast players using AirPlay.

## Setup

  1. [Install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html). The easiest way (especially on Pi or a Debian system) is via Pip:
     1. (If on Pi/Debian): `sudo apt-get install -y python3-pip`
     2. (Everywhere): `pip3 install ansible`
  2. Clone this repository: `git clone https://github.com/martinbrose/home-pi.git`, then enter the repository directory: `cd home-pi`.
  3. Install requirements: `ansible-galaxy collection install -r requirements.yml` (if you see `ansible-galaxy: command not found`, restart your SSH session or reboot the Pi and try again)
  4. Make copies of the following files and customize them to your liking:
     - `example.inventory.ini` to `inventory.ini` (replace IP address with your Pi's IP, or comment that line and uncomment the `connection=local` line if you're running it on the Pi you're setting up).
     - `example.config.yml` to `config.yml`
  5. Run the playbook: `ansible-playbook main.yml`

## Usage

### Home Assistant

Visit the Pi's IP address (e.g. http://192.168.1.10:8123/).

## Inspired by

This project is inspired and based on the excellent [Internet Pi](https://github.com/geerlingguy/internet-pi).<br>
Check it out for a Raspberry Pi Configuration for Internet connectivity.

## License

MIT

## Author

This project was created in 2022 by Martin Brose.
