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


$ sudo add-apt-repository ppa:graphics-drivers/ppa  
$ sudo apt update  
$ sudo ubuntu-drivers autoinstall  
$ sudo reboot  


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
https://velog.io/@t1won/Ubuntu-%EC%9A%B0%EB%B6%84%ED%88%AC-%ED%95%9C%EA%B8%80-%EC%9E%85%EB%A0%A5-%EB%B0%8F-%ED%95%9C%EC%98%81%ED%82%A4-%EC%84%A4%EC%A0%95

# terminator 설치  
sudo apt-get install terminator

# 아나콘다 설치  
https://ieworld.tistory.com/12
