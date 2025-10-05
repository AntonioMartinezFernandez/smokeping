# smokeping

ping monitoring with smokeping

# Getting Started

Execute the following command to start a smokeping container:

```bash
docker run -d \
  --name=smokeping \
  --hostname=smokeping \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -p 8080:80 \
  -v ./config:/config \
  -v ./data:/data \
  --restart unless-stopped \
  lscr.io/linuxserver/smokeping:latest
```

Then access `http://localhost:8080/smokeping/` in your browser.
