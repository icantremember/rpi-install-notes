https://github.com/azlux/log2ram

add the repo  
```echo "deb [signed-by=/usr/share/keyrings/azlux-archive-keyring.gpg] http://packages.azlux.fr/debian/ bookworm main" | sudo tee /etc/apt/sources.list.d/azlux.list```  
```sudo wget -O /usr/share/keyrings/azlux-archive-keyring.gpg  https://azlux.fr/repo.gpg```  

update and install  
```sudo apt update```  
```sudo apt install log2ram```
