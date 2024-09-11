### story-upde-README.md
## Upgrade Your Node To New Version 0.9.12
- Stop Node First

```sh sudo systemctl stop story```

# Download Binanry

```sh wget https://story-geth-binaries.s3.us-west-1.amazonaws.com/story-public/story-linux-amd64-0.9.12-9ae4a63.tar.gz
tar -xzvf story-linux-amd64-0.9.12-9ae4a63.tar.gz
[ ! -d "$HOME/go/bin" ] && mkdir -p $HOME/go/bin
if ! grep -q "$HOME/go/bin" $HOME/.bash_profile; then
  echo 'export PATH=$PATH:$HOME/go/bin' >> $HOME/.bash_profile
fi
sudo cp story-linux-amd64-0.9.12-unstable-9ae4a63/story $HOME/go/bin/story
source $HOME/.bash_profile
story version```


# Reload & Start Service

```sh sudo systemctl daemon-reload && \
sudo systemctl start story && \
sudo systemctl enable story && \
sudo systemctl status story```

# Check Log

```sh sudo journalctl -u story -f -o cat ```
  
