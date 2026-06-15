# niisama
install
wget https://github.com/bitwarden/clients/releases/download/cli-v2026.4.2/bw-linux-2026.4.2.zip
unzip bw-linux-2026.4.2.zip
chmod +x bw
sudo mv bw /usr/local/bin/



Log in to the Bitwarden web vault.
Go to Settings → Security → Keys.
Create or view your Client ID and Client Secret.
In Linux:
export BW_CLIENTID="xxxx"
export BW_CLIENTSECRET="yyy"
bw login --apikey

bw unlock
export BW_SESSION="..."
export BW_SESSION=$(bw unlock --raw)
bw list items
