# 학교 네트워크 설정

cd /etc/netplan/

거기 파일 하나 있는거 편집

sudo gedit 하고 tab으로 파일이름 자동완성 후 엔터.   
![44](https://user-images.githubusercontent.com/40755420/145689717-8ea0c46e-958f-42fa-813a-5aeb02a3a658.png)



위와 같이 설정하되 addresses바로 밑 한줄만 자기 본체에 적힌 ip주소로 바꾸기

save후 메모장 끄고

sudo netplan apply

오류 없으면 sudo reboot

오류는 보통 스페이스바 갯수차이 잘 보고 할 것

# 서버 변경
  
https://ieworld.tistory.com/8


# 그래픽카드 잡기


~~$ sudo add-apt-repository ppa:graphics-drivers/ppa  
$ sudo apt update 
$ sudo ubuntu-drivers autoinstall  
$ sudo reboot~~  

설치가능 드라이버 확인 
```
ubuntu-drivers devices
```

자동으로 설치
```
sudo ubuntu-drivers autoinstall
```

원하는 버전 설치
```
sudo apt install nvidia-driver-470
```  
Nvidia kernel module load 도와주는 modprobe 패키지 설치
```
sudo apt-get install dkms nvidia-modprobe
```

마무리
```
sudo apt update
sudo apt upgrade

sudo reboot
```
출처 : https://ingu627.github.io/tips/install_cuda_linux/  

# teamviewer 설치  

wget https://download.teamviewer.com/download/linux/teamviewer_amd64.deb   
sudo apt install ./teamviewer_amd64.deb   

20.04 는 아래 링크글 보고 따라하기
https://www.bddungsblog.com/2021/02/ubuntu-2004-how-to-install-teamviewer.html

## teamviewer 자동실행
1. 서비스를 실행 할 스크립트 작성.

  - 위치 : /etc/init.d/[사용자 실행스크립트 생성]

  ex : /etc/init.d/auto_run.sh

  - 자동 실행 등록을 하면 해당 스크립트가 실행되어 서비스를 띄우게 된다.



2. 권한 부여

  - chmod 777 /etc/init.d/[실행 스크립트이름]

  - ex : chmod 777 /etc/init.d/auto_run.sh



3. 서비스 등록

  - update-rc.d [실행 스크립트 이름] defaults

  ex : update-rc.d auto_run.sh defaults

  

  defaults : runlevel 3, 5



4. 확인 

  - 재부팅하여 서비스 확인

https://sbgg.tistory.com/28


# 한글 입력기 설치
https://greedywyatt.tistory.com/105  
https://shanepark.tistory.com/231

# 글카 설치후 인터넷 안될때   
https://velog.io/@sim0297/ubuntu-nvidia-driver-%EC%84%A4%EC%B9%98-%EC%8B%9C-%EB%9E%9C%EC%B9%B4%EB%93%9C-%EC%9D%B8%EC%8B%9D%EC%95%88%EB%90%98%EB%8A%94-%EC%98%A4%EB%A5%98

# terminator 설치  
sudo apt-get install terminator

# 아나콘다 설치  
https://ieworld.tistory.com/12

# Grub 수정  
http://programmingskills.net/grub%EC%9D%98-%EB%8C%80%EA%B8%B0-%EC%8B%9C%EA%B0%84-%EA%B8%B0%EB%B3%B8-%EB%B6%80%ED%8C%85-%EC%88%9C%EC%84%9C-%EB%B0%94%EA%BE%B8%EA%B8%B0/

