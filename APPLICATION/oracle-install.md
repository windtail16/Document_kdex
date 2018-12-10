
### Install oracle instant client rpm 

```sh
sudo apt install alien
sudo alien -i oracle-instantclient12.2-basic-12.2.0.1.0-1.x86_64.rpm
sudo alien -i oracle-instantclient12.2-devel-12.2.0.1.0-1.x86_64.rpm
sudo apt install libaio1
```

### 라이브 러리 패스 설정

```sh
sudo vi /etc/ld.so.conf.d/oracle.conf && sudo chmod o+r /etc/ld.so.conf.d/oracle.conf
```
아래의 url을 추가

```
/usr/lib/oracle/12.2/client64/lib/
```

아래 명령어 실행

```sh
sudo ldconfig
```