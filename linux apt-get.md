|구분 |명령어|
|:----------:|:--|
|업데이트 |apt-get update|
|Git|apt-get install git|
| (Check)  |git version   |
|geth   |git clone -b release/1.3.6 https://github.com/ethereum/go-ethereum.git   |
|Go언어| sudo apt-get install -y build-essential libgmp3-dev golang|
| geth build |make -C go-ethereum geth|
| (Check)  |./go-ethereum/build/bin/geth version   |
|Path 추가|cp go-ethereum/build/bin/geth /usr/bin/|
|(Check)|geth version|
||mkdir BlockChain01|

**도커에서는 vi쓰려면 vim설치해줘야한다.**
(원래 리눅스에서 vi설치해야하는지는 몰겟다ㅋㅋ)
스택오버플로우에서는 vim을 설치하란다.
apt-get install -y vim

**net-tools 설치**

netstat , ifconfig 사용가능

apt-get install net-tools

**SSH 설치**

apt-get install -y openssh-server

포트변경 vi /etc/ssh/sshd_config -> Port 8022(임의)

service ssh restart

netstat -an


### geth

mkdir BlockChain01

cd BlockChain01

vim genesis01.txt

mv genesis01.txt genesis01.json
