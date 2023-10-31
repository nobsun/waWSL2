# 'DNS issues in WSL2' 問題の回避策

0. WSLのアップデート
1. `nkf` をインストール
```
sudo apt install nkf
```
2. `wsl.conf` を `/etc/` にコピー
    ```
    sudo cp wsl.conf /etc/
    ```
3. `set-resolv-conf` スクリプトを `/usr/local/bin/` にコピー
    ```
    chmod +x set-resolv-conf
    sudo cp set-resolv-conf /usr/local/bin/
    ```
4. `set-resolv-conf.service` を `/etc/systemd/system/` にコピー
    ```
    sudo cp set-resolv-conf.service /etc/systemd/system/
    ```
5. `set-resolv-conf.service` の有効化
    ```
    sudo systemctl enable set-resolv-conf
    ```
6. WSLの再起動

