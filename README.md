# macsible

Inspired by Adam Chainz's ansible repo: https://github.com/adamchainz/mac-ansible
He has a great page explaining this little deployment as well: https://adamj.eu/tech/2019/03/20/how-i-provision-my-macbook-with-ansible/

Only bug I came across with ansible homebrew module is some packages are installed on the remote computer but not accessable.
ex: microsoft-office is installed on remote machine. When you do "brew cask install microsoft-office" on the remote box you get "package already installed" message. It only installs when you do "brew cask reinstall microsoft-office". I checked and homebrew_cask has an option to use force "install_options: force". That may work.
