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





# 그래픽카드 잡기


$ sudo add-apt-repository ppa:graphics-drivers/ppa
$ sudo apt update
$ sudo ubuntu-drivers autoinstall
$ sudo reboot


# teamviewer 설치  

wget https://download.teamviewer.com/download/linux/teamviewer_amd64.deb   
sudo apt install ./teamviewer_amd64.deb   


# 한글 입력기 설치
https://greedywyatt.tistory.com/105
