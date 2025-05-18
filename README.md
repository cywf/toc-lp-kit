# toc-lp-kit

**Tactical Operations Center – Listening Post Kit**  
A self-contained, dockerized HF digital receive node.  Build and deploy on a single Ubuntu host (e.g., Raspberry Pi Node + RTL-SDR v4) to decode JS8Call traffic and log new station sightings.

## Quick Start

1. **Clone**  
```bash
git clone https://github.com/cywf/toc-lp-kit.git
cd toc-lp-kit
```

2. **Configure USB Access**
```bash
echo 'blacklist dvb_usb_rtl28xxu' | sudo tee /etc/modprobe.d/rtl.conf
sudo reboot
```

3. **Bring up services**
```bash
docker-compose up -d
```

4. **Launch JS8Call GUI** (_on the host’s desktop_)
•	Audio is already piped from SDR into the container
•	Monitor decoded messages in real time

---

## What’s Inside
•	chrony – containerized time sync
•	sdr-pipeline – rtl_fm → sox → PulseAudio
•	js8call – JS8Call GUI & decoder
•	docker-compose.yml – orchestration of all services

## License
This project is MIT-licensed. See [LICENSE](https://github.com/cywf/toc-lp-kit/blob/main/LICENSE).
