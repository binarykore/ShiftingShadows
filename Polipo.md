# InstallationSetup of Polipo

apt-get install polipo -y

service polipo stop

polipo socksParentProxy=127.0.0.1:1080

git config --global http.proxy 18.188.40.53:8080

http_proxy=http://18.188.40.53:8080 ping www.google.com

service polipo restart

nano ~/.bashrc

alias fisher = "polipo -c ~/.poliporc"

or save as .sh

echo "polipo -c ~/.poliporc" > service.sh

source ~/.bashrc
