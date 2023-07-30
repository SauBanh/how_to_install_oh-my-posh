# how_to_install_oh-my-posh
## with wsl
### 
### step 1 install unzip
```c
sudo apt-get install unzip
```
### step 2 update
```c
sudo apt update
```
### step 3 install curl
```c
sudo apt install curl
```
### step 4 install ohmyposh
```c
curl -s https://ohmyposh.dev/install.sh |sudo bash -s
```
### step 5 check ohmyposh
```c
oh-my-posh
```
### step 6 create a folder containing the theme
```c
mkdir ~/.poshthemes
```
### step 7 copy the theme you want to use and replace it with `<yourtheme>` (you can choice theme <a href="https://ohmyposh.dev/docs/themes">in here</a>)
```c
sudo cp /root/themes/<yourtheme>.omp.json ~/.poshthemes/
```
### step 8 show theme you will use
```c
ls ~/.poshthemes
```
### step 9 run this command debug, if success go to next step
```c
sudo oh-my-posh debug --config ~/.poshthemes/<yourtheme>.omp.json
```
### step 10 next to change the access permission of the path
```c
sudo chown tuananhdev /home/tuananhdev/.poshthemes/<yourtheme>.omp.json
```
### step 11 run this command to see the change
```c
eval "$(oh-my-posh init bash --config ~/.poshthemes/<yourtheme>.omp.json)"
```
### Now you need to save the configuration so that every time you open the terminal the theme will automatically appear.Use this command to move file bashrc
```c
sudo nano ~/.bashrc
```
### step 12 use the down button on your keyboard to move to the bottom and add the below command at the end
```c
eval "$(oh-my-posh init bash --config ~/.poshthemes/<yourtheme>.json)"
```
### now ctrl + s to save and ctrl + x to exit
### Next you need to install the font. <a href="https://www.nerdfonts.com/font-downloads">Click here</a> to choice font.After downloading the font, install it on your computer
### The last step, you go to the settings by clicking the button next to create a new tab and select settings. At the taskbar select the ubuntu just installed and find the interface. find font-face and change the font you just installed. Save the settings again and you're done
## good luck

# Install with windowns
```terminal
Set-ExecutionPolicy RemoteSigned
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
//to set theme 
notepad $PROFILE
```
change PROFILE
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\night-owl.omp.json" | Invoke-Expression
