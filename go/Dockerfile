# this file describes how to build tsuru go image
# to run it:
# 1 - tsuru-admin platform-add go -d https://raw.github.com/tsuru/basebuilder/master/go/Dockerfile

from    docker.cn/docker/ubuntu:14.04
run echo "deb http://mirrors.sohu.com/ubuntu/ trusty main restricted universe multiverse" > /etc/apt/sources.list
run echo "deb http://mirrors.sohu.com/ubuntu/ trusty-security main restricted universe multiverse" >> /etc/apt/sources.list
run echo "deb http://mirrors.sohu.com/ubuntu/ trusty-updates main restricted universe multiverse" >> /etc/apt/sources.list
run echo "deb http://mirrors.sohu.com/ubuntu/ trusty-proposed main restricted universe multiverse" >> /etc/apt/sources.list
run echo "deb http://mirrors.sohu.com/ubuntu/ trusty-backports main restricted universe multiverse" >> /etc/apt/sources.list
run	apt-get update
run	apt-get install wget -y --force-yes
run	wget https://codeload.github.com/danielfree/basebuilder/legacy.tar.gz/master -O basebuilder.tar.gz --no-check-certificate
run	mkdir /var/lib/tsuru
run	tar -xvf basebuilder.tar.gz -C /var/lib/tsuru --strip 1
run	cp /var/lib/tsuru/go/deploy /var/lib/tsuru
run	cp /var/lib/tsuru/go/start /var/lib/tsuru
run	/var/lib/tsuru/go/install
