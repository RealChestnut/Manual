Moudular_Airial_Drone_Manuel
============================

1. ROS melodic Installing and Configuring Environment(Upboard) 
2. Moudlar_Airial_Drone_Package_review(shit)


# 1. ROS melodic Installing and Configuring Environment(Upboard) 
  
 ## * Ubuntu 18.04 다운로드
    
    1. 업보드의 경우도 데스크탑과 동일하게 usb나 sd카드를 통해 iso파일을 이동저장장치에 굽습니다.
       
       우분투 18.04버전으로 다운받습니다.
       
       
       
       
       -  https://releases.ubuntu.com/bionic/ 링크에 접속해서 iso 파일을 다운받습니다.
       -  https://www.balena.io/etcher/ 링크에 접속해서 etcher 파일(Download for Window x84|x64)을 다운로드 받습니다.
       -     
       
       
       
       After the reboot you need to add our repository:

       sudo add-apt-repository ppa:aaeon-cm/5.4-upboard

       Update the repository list

       sudo apt update

       Remove all the generic installed kernel (select No on the question "Abort Kernel Removal")

       sudo apt-get autoremove --purge 'linux-.*generic'

       Install our kernel(18.04 and 20.04 share the same 5.4 kernel):

       sudo apt-get install linux-generic-hwe-18.04-5.4-upboard

       Install the updates:

       sudo apt dist-upgrade -y

       sudo update-grub

       Reboot

       sudo reboot

       After the reboot, you can verify that the kernel is indeed installed by typing

       
       
       
       ※ 설치하는 동안 "automatic updates" 옵션은 체크해제해 주세요
       ※ 마이크로컨트롤러 수업에서 활용한 rufus와 같은 매체가 아닌 etcher라는 프로그램을 활용합니다.
       ※ https://www.youtube.com/watch?v=Wh239HUfYI8 참조자료 링크
    
    2. 이미 설치된 우분투가 오작동하는 경우 포맷을 진행합니다. 
       
       데스크탑 환경에서와 달리 업보드 환경에서는 우분투만 설치되어 있습니다.
       그런 이유로 우분투 환경 내에서 포맷을 진행합니다.
       포맷과정은 다음의 링크를 참조해 주세요 
       
       https://www.ubuntubuzz.com/2020/02/how-to-format-disk-drive-with-ubuntu-disk-utility.html 
       
       - 우분투 메뉴창에 disk를 검색해 들어간뒤 
       - 시스템파일이 저장된 drive를 선택하여 포맷을 진행합니다.
       
    3. 우분투 설치가 끝났다면 ROS를 다운받습니다. 
      
       
       
       
     
  
     
    
    
