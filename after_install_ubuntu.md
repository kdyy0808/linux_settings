학교 네트워크 설정

cd /etc/netplan/

거기 파일 하나 있는거 편집

sudo gedit 하고 tab으로 파일이름 자동완성 후 엔터




위와 같이 설정하되 addresses바로 밑 한줄만 자기 본체에 적힌 ip주소로 바꾸기

save후 메모장 끄고

sudo netplan apply

오류 없으면 sudo reboot

오류는 보통 스페이스바 갯수차이 잘 보고 할 것





그래픽카드 잡기



