Moudular_Airial_Drone_Manuel
============================

1. ROS melodic Installing and Configuring Environment(Upboard) 
2. Download drone packages developed
3. Moudlar_Airial_Drone_Package_review(shit)


# 1. ROS melodic Installing and Configuring Environment(Upboard) 
  
 ## * Ubuntu 18.04 다운로드
    
    1. 업보드의 경우도 데스크탑과 동일하게 usb나 sd카드를 통해 iso파일을 이동저장장치에 굽습니다.
       
       우분투 18.04버전으로 다운받습니다.
       
       
       
       
       -  https://releases.ubuntu.com/bionic/ 링크에 접속해서 64-bit PC (AMD64) desktop image 파일을 다운받습니다.
       -  https://www.balena.io/etcher/ 링크에 접속해서 etcher 파일(Download for Window x84|x64)을 다운로드 받습니다.
       -  다운받은 image파일을 etcher에 넣고 start를 눌러 이미지를 굽습니다. 
       -  구운 이미지 파일을 업보드에 연결한 뒤 업보드를 실행하면 나오는 install ubuntu를 눌러 다운로드 받습니다.
       -  그 다음은 터미널 창을 열어 업보드만의 우분투 커널을 다운받습니다. 다음의 코드를 차례대로 입력하세요

          sudo add-apt-repository ppa:aaeon-cm/5.4-upboard
          
          sudo apt update
          
          sudo apt-get autoremove --purge 'linux-.*generic'
          
          sudo apt-get install linux-generic-hwe-18.04-5.4-upboard
          
          sudo apt dist-upgrade -y
          
          sudo update-grub
          
          sudo reboot (꺼졌다고 놀라지 마세요 재부팅하는 겁니다.)


       ※ 우분투를 설치하는 동안 "automatic updates" 옵션은 체크해제해 주세요
       ※ 마이크로컨트롤러 수업에서 활용한 rufus와 같은 매체가 아닌 etcher라는 프로그램을 활용합니다.
       ※ https://www.youtube.com/watch?v=Wh239HUfYI8 우분투 설치 참조자료 링크 커널 설치 전까지만 참조하세요
       ※ https://github.com/up-board/up-community/wiki/Ubuntu_18.04 우분투 커널 설치 wiki
    
    2. 이미 설치된 우분투가 오작동하는 경우 포맷을 진행합니다. 
       
       데스크탑 환경에서와 달리 업보드 환경에서는 우분투만 설치되어 있습니다.
       그런 이유로 우분투 환경 내에서 포맷을 진행합니다.
       포맷과정은 다음의 링크를 참조해 주세요 
       
       https://www.ubuntubuzz.com/2020/02/how-to-format-disk-drive-with-ubuntu-disk-utility.html 
       
       - 우분투 메뉴창에 disk를 검색해 들어간뒤 
       - 시스템파일이 저장된 drive를 선택하여 포맷을 진행합니다.
       
    3. 우분투 설치가 끝났다면 ROS를 다운받습니다.
    
       다음의 설치과정을 따라 코드를 진행해 주세요.
      
      - 소스 리스트 셋업 
        sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
      
      - key 셋업
        sudo apt install curl # curl이 설치되지 않았다면 설치해 주세요
        curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
        
      - 설치
        sudo apt update
        
        sudo apt install ros-melodic-desktop-full
        
      - 환경설정
        
        echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
        source ~/.bashrc
        
        sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
        
        sudo apt install python-rosdep
        
        sudo rosdep init
        
        rosdep update
        
       
      - 단축키 설정
        
        배쉬 파일을 열었을때의 환경을 다음과 같이 바꿔주세요(편의를 위함)
        
        xxx.xxx.xxx.xxx 는 자신의 IP

        gedit ~/.bashrc
        
        # set ROS melodic
        source /opt/ros/indigo/setup.bash
        source ~/catkin_ws/devel/setup.bash

        # set ROS Network
        export ROS_MASTER_URI=http://xxx.xxx.xxx.xxx:11311
        export ROS_HOSTNAME=xxx.xxx.xxx.xxx

        # set ROS alias command
        alias cw='cd ~/catkin_ws'
        alias cs='cd ~/catkin_ws/src'
        alias cm='cd ~/catkin_ws && catkin_make'
        
# 2. Download drone packages developed 
  
  ## * 깃허브에서 패키지 가져오기 
  
    1. ㅇㄹㅇㄹ
  

      
      
    
      
      
       
       
       
     
  
     
    
    
