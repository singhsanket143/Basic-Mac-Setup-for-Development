
```markdown
# macOS Development Environment Setup

## 1. Foundation
```bash
# Install Xcode Command Line Tools
xcode-select --install

# Install Homebrew
/bin/bash -c "$(curl -fsSL [https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh](https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh))"

# Update Homebrew
brew update

```

## 2. Runtimes & Languages

### Node.js & React

```bash
brew install nvm
mkdir ~/.nvm
nvm install --lts

```

### Java (Spring Boot)

```bash
brew install openjdk@17 -- for java 17
brew install openjdk@21 -- for java 21
brew install maven
brew install gradle

```

### Python, Go, & C++

```bash
brew install python
brew install go
brew install gcc
brew install cmake

```

## 3. Databases

### MySQL

```bash
brew install mysql
brew services start mysql
mysql_secure_installation

```

### MongoDB

```bash
brew tap mongodb/brew
brew install mongodb-community
brew services start mongodb-community

```

## 4. Applications (Casks)

```bash
brew install --cask visual-studio-code
brew install --cask docker
brew install --cask postman
brew install --cask dbeaver
brew install --cask iterm2

```

## 5. Git Configuration

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
ssh-keygen -t ed25519 -C "your.email@example.com"

```

## 6. Environment Configuration (ZSH)

Run these to ensure your system recognizes the new installations:

```bash
echo 'export PATH="/usr/local/opt/openjdk@17/bin:$PATH"' >> ~/.zshrc
echo 'export NVM_DIR="$HOME/.nvm"' >> ~/.zshrc
echo '[ -s "/usr/local/opt/nvm/nvm.sh" ] && . "/usr/local/opt/nvm/nvm.sh"' >> ~/.zshrc
source ~/.zshrc

```
