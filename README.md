# zsh_to_fish
How to make zsh like fish?


## 1. Install [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh).
```
cd && sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## 2. Clone necessary plugins.
### a. [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
```
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
```
### b. [zsh-history-substring-search](https://github.com/zsh-users/zsh-history-substring-search)
```
git clone https://github.com/zsh-users/zsh-history-substring-search.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search
```
### c. [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

## 3. Add plugins to `~/.zshrc`
```
plugins = ( [plugins...] zsh-autosuggestions history-substring-search zsh-syntax-highlighting)
```
Note: make sure zsh-syntax-highlighting is the last one in the above list.

## 4. Restart zsh
```
source ~/.zshrc
```
