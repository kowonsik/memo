#### Linux Serial Port

```sh

dmesg | grep tty

# 부팅시 커널에 내장된 각 장치 드라이버가 해당 하드웨어를 탐색한다
# dmesg 명령어로 커널의 메시지 버퍼를 출력한다

```

```sh
# pyserial install
wget http://sourceforge.net/projects/pyserial/files/pyserial/2.7/pyserial-2.7.tar.gz
tar xvfz pyserial-2.7.tar.gz
cd pyserial-2.7
python setup.py install

```


#### Bitnami wordpress
https://wiki.bitnami.com/applications/bitnami_wordpress_stack

##### restart server

```sh

/opt/wordpress-4-2.2-2/appache2/scripts/
./ctl.sh start

```
