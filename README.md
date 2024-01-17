
## Starship
### CROSS-SHELL-PROMPT

![App Screenshot](https://raw.githubusercontent.com/starship/starship/master/media/demo.gif)


#### The minimal, blazing-fast, and infinitely customizable prompt for any shell!

 - Fast: it's fast – really really fast! 🚀
 - Customizable: configure every aspect of your prompt.
 - Universal: works on any shell, on any operating system.
 - Intelligent: shows relevant information at a glance.
 - Feature-rich: support for all your favorite tools.
 - Easy: quick to install – start using it in minutes.

## 🚀 Installation
### Prerequisites

- A [Nerd Font](https://www.nerdfonts.com/) installed and enabled in your terminal (for example, try the [FiraCode Nerd Font](https://www.nerdfonts.com/font-downloads)

### Step 1. Install Starship
Select your operating system from the list below to view installation instructions:

- #### Linux:
#### First, install curl:
- Ubuntu/Mint:
```
sudo apt install curl
```
- Fedora:
```
sudo dnf install curl
```
- Manjaro/Arch:
```
sudo pacman -S curl
```

Then Install the latest version for your system:
```
curl -sS https://starship.rs/install.sh | sh
```
#### Alternatively, install Starship using any of the following package managers: 

| **Distribution**   | **Instructions**                                                     |
|--------------------|----------------------------------------------------------------------|
| Any                | ``` cargo install starship --locked  ```                             |
| Any                | ``` conda install -c conda-forge starship  ```                       |
| Any                | ``` brew install starship  ```                                       |
| Alpine Linux 3.13+ | ``` apk add starship  ```                                            |
| Arch Linux         | ``` pacman -S starship  ```                                          |
| CentOS 7+          | ``` dnf copr enable atim/starship  ``` ``` dnf install starship  ``` |
| Gentoo             | ``` emerge app-shells/starship  ```                                  |
| Manjaro            | ``` pacman -S starship  ```                                          |
| NixOS              | ``` nix-env -iA nixpkgs.starship  ```                                |
| openSUSE           | ``` zypper in starship  ```                                          |
| Void Linux         | ``` xbps-install -S starship  ```                                    |

- #### MacOS
Install the latest version for your system:
```
curl -sS https://starship.rs/install.sh | sh
```

- #### Windows
Install the latest version for your system with the MSI-installers from the [releases section](https://github.com/starship/starship/releases/tag/v1.17.1).

Install Starship using any of the following package managers:

| **Repository** | **Instructions**                               |
|----------------|------------------------------------------------|
| [crates.io](https://crates.io/crates/starship)      | ``` cargo install starship --locked  ```       |
| [Chocolatey](https://community.chocolatey.org/packages/starship)     | ``` choco install starship  ```                |
| [conda-forge](https://anaconda.org/conda-forge/starship)    | ``` conda install -c conda-forge starship  ``` |
| [Scoop](https://github.com/ScoopInstaller/Main/blob/master/bucket/starship.json)          | ``` scoop install starship  ```                |
| [winget](https://github.com/microsoft/winget-pkgs/tree/master/manifests/s/Starship/Starship)         | ``` winget install --id Starship.Starship  ``` |

###  Step 2. Set up your shell to use Starship
Configure your shell to initialize starship. Select yours from the list below:

- #### Bash
Add the following to the end of ```~/.bashrc```:
```
eval "$(starship init bash)"
```

- #### Cmd
You need to use [Clink](https://chrisant996.github.io/clink/clink.html) (v1.2.30+) with Cmd. Create a file at this path ``` %LocalAppData%\clink\starship.lua ``` with the following contents:
```
load(io.popen('starship init cmd'):read("*a"))()
```
- #### Fish
Add the following to the end of ``` ~/.config/fish/config.fish ```:

```
starship init fish | source
```

- #### Nushell
Add the following to the end of your Nushell env file (find it by running ``` $nu.env-path ``` in Nushell):
```
mkdir ~/.cache/starship
starship init nu | save -f ~/.cache/starship/init.nu

```
And add the following to the end of your Nushell configuration (find it by running ``` $nu.config-path ``` ):
```
use ~/.cache/starship/init.nu
```
- #### PowerShell
Add the following to the end of your PowerShell configuration (find it by running ``` $PROFILE ``` ):
```
Invoke-Expression (&starship init powershell)
```
- #### Zsh
Add the following to the end of ``` ~/.zshrc ```:

```
eval "$(starship init zsh)" 
```

###  Step 3. Configure Starship

Start a new shell instance, and you should see your beautiful new shell prompt. If you're happy with the defaults, enjoy!

If you're looking to further customize Starship:

#### You can use my advanced config file
To get started configuring starship, create the following file: ``` ~/.config/starship.toml ```.
```
~/.config && touch ~/.config/starship.toml && sudo nano starship.toml
```
Then visit my [Advance config file](https://gist.github.com/azmarifdev/7a3bc1a098ce5eca1dfedae7f336cc82) and copy all config lines. then paste in ``` starship.toml ``` file and save it.

Follow this shortcut if you don't know how to save and exit the nano file.

(Press Ctrl + O then Press Enter to Save And Press Ctrl + X to Exit)

#### Official Documents
- [Starship Docs](https://starship.rs/)
- [Configuration](https://starship.rs/config/) – learn how to configure Starship to tweak your prompt to your liking
- [Presets](https://starship.rs/presets/) – get inspired by the pre-built configuration of others

