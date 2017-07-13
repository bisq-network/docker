# Bisq-Docker
Docker build for Bisq/Bitssquare

```git clone https://github.com/cedricwalter/Bisq-Docker.git && cd Bisq-Docker```

# Build
```sudo docker build -t bisq-0.5.2 .```

# Run
You may want to mount the bisq data directory on your host for easier upgrades
```sudo docker run -v $PWD/data:/root/.local/share/bisq -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=unix$DISPLAY bisq-0.5.2```

# Bisq data directory
Read also CAREFULLY https://github.com/bitsquare/bitsquare/wiki/Switching-to-a-new-data-directory
