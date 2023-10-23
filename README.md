# 'DNS issues in WSL2' 問題の回避策

1. `wsl.conf` を `/etc/` にコピー
    ```
    $ sudo cp wsl.conf /etc/
    ```
2. `set-resolv-conf` スクリプトを `/usr/local/bin/` にコピー
    ```
    $ sudo cp set-resolv-conf /usr/local/bin/
    ```
3. `set-resolv-conf.service` を `/etc/systemd/system/` にコピー
    ```
    $ sudo cp set-resolv-conf.service /etc/systemd/system/
    ```
4. `set-resolv-conf.service` の有効化
    ```
    $ cd /etc/systemd/system/
    $ sudo systemctl enable set-resolv-conf
    ```
5. WSLの再起動

