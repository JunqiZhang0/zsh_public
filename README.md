#### Instruction 
###### step1 :
```bash
sudo yum install zsh
sudo usermod -s $(which zsh) $(whoami) #This will change the default terminal to zsh for the current user
```
###### step2: install oh-my-zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
sudo reboot #or you can logout and login back, it should also work
```
###### step3: download the plugins
```bash
#download the plugins
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
source ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions/zsh-autosuggestions.zsh
git clone git://github.com/wting/autojump.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/autojump
source ~/.oh-my-zsh/custom/plugins/autojump/autojump.zsh
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
source ~/.oh-my-zsh/custom/plugins/syntax-highlighting/syntax-highlighting.zsh
```
###### step4:
```bash
cp ./zshconfig/zsh_template ~/.zshrc
```
###### step 5 (optional):
```bash
cp .zshconfig/p10k_template ~/.p10k.zsh
```

(For macos, you need to choose hack regular nerd font complete mono, run 
```bash
brew tap homebrew/cask-fonts
brew cask install font-hack-nerd-font
```
to install fonts
)
