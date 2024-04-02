# HackPack
1. Clone repo
```
sudo mkdir /usr/local/bin/hackpack
git clone https://github.com/bgutowski/HackPack.git /usr/local/bin/hackpack
```

2. Edit .zshrc
```
cat <<EOT >> ~/.zshrc
function _hackpack_completion() {
  _files -W /usr/local/bin/HackPack -g 'hackpack-*'
}

function hackpack() {
  cat /usr/local/bin/HackPack/$1
}

compdef _hackpack_completion hackpack
EOT
```

3. Reload .zshrc
```
source ~/.zshrc
```
