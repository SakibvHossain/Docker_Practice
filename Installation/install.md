# Installation process only applicable for win 10 pro or 11 pro version 22H2
### Suppose you don't know anything about docker. So let's install without knowing it :D

### Installing process
**Step - 1:** Install  Docker desktop [Click here](https://docs.docker.com/desktop/install/windows-install/)   
  
**Step - 2:** WSL version 1.1.3.0 or later means that you need to install WSL (Windows Subsystem for Linux). Win 10 pro or 11 pro has pre-installed Linux distribution. So you can now install WSL from microsoft store. Search for linux you'll get **kali**, **ubuntu**, **oracle linux**. I downloaded ubuntu LTS because I saw people having problem with other WSL.  
  
**Step - 3:** Just run your Docker desktop and your done.  
  
  

### Check
Open `cmd` type `docker -v` hit enter and see the docker version.  
  
**Having problem?**  
Set the path to system veriable `C:\Program Files\Docker\Docker\resources\bin` then  check again.
