#### mac에서 oracle 접속(python : cx_Oracle)

```sh

# python library download
# cx_Oracle SourceCode : http://cx-oracle.sourceforge.net
# Oracle Instant Basic 64-bit : http://www.oracle.com/technetwork/topics/intel-macsoft-096467.html
# Oracle Instant Client SDK 64-bit : http://www.oracle.com/technetwork/topics/intel-macsoft-096467.html

sudo su
mkdir /Users/유저네임/orcle
mv /Users/유저네임/Downloads/instantclient-* /Users/유저네임/oracle

cd /Users/유저네임/oracle/
unzip instantclient-basic-macos.x64-11.2.0.3.0.zip
unzip instantclient-sdk-macos.x64-11.2.0.3.0.zip
cd instantclient_11_2/sdk
unzip ottclasses.zip

cd ..
cp -R ./sdk/* ./
cp -R ./sdk/include/* ./
ln -s libclntsh.dylib.11.1 libclntsh.dylib
ln -s libocci.dylib.11.1 libocci.dylib
vim ~/.bash_profile

```

```sh
export ORACLE_HOME=/Users/유저네임/oracle/instantclient_11_2
export DYLD_LIBRARY_PATH=$ORACLE_HOME
export LD_LIBRARY_PATH=$ORACLE_HOME

```

```sh
# 확인

. ~/.bash_profile
echo $ORACLE_HOME 
echo $DYLD_LIBRARY_PATH 
echo $LD_LIBRARY_PATH

which python # usually /usr/bin/python
which gcc # usually /usr/bin/gcc

```

```sh

. ~/.bash_profile
cd /Users/유저네임/Downloads
tar -xzf cx_Oracle-5.1.2.tar.gz
cd cx_Oracle-5.1.2

sudo python setup.py build
sudo python -E setup.py install

```


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
