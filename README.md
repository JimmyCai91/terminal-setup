# terminal-setup

<br>

## ZSH

1. Install ZSH
    ``` bash
    sudo apt install zsh
    ```
   
2. Install Oh My Zsh
    ``` bash
   sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)" 
   ```

3. Install ZNAP

    Using Znap to manage your plugins can be as simple as putting this in your `.zshrc` file:
    ```zsh
    # Download Znap, if it's not there yet.
    [[ -f ~/Git/zsh-snap/znap.zsh ]] ||
        git clone --depth 1 -- \
            https://github.com/marlonrichert/zsh-snap.git ~/Git/zsh-snap

    source ~/Git/zsh-snap/znap.zsh  # Start Znap

    # `znap prompt` makes your prompt visible in just 15-40ms!
    znap prompt sindresorhus/pure

    # `znap source` automatically downloads and starts your plugins.
    znap source marlonrichert/zsh-autocomplete
    znap source zsh-users/zsh-autosuggestions
    znap source zsh-users/zsh-syntax-highlighting

    # `znap eval` caches and runs any kind of command output for you.
    znap eval iterm2 'curl -fsSL https://iterm2.com/shell_integration/zsh'

    # `znap function` lets you lazy-load features you don't always need.
    znap function _pyenv pyenvn 'eval "$( pyenv init - --no-rehash )"'
    compctl -K    _pyenv pyenv
    ```
    Update `.zshrc`, then in terminal run:
    ```bash
    $ zsh
    $ source ~/.zshrc
   ```
