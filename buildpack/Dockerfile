from    progrium/buildstep
run     apt-get update
run     apt-get install wget sudo -y --force-yes
run     wget http://github.com/tsuru/basebuilder/tarball/master -O basebuilder.tar.gz --no-check-certificate
run     mkdir /var/lib/tsuru
run     tar -xvf basebuilder.tar.gz -C /var/lib/tsuru --strip 1
run     cp /var/lib/tsuru/buildpack/deploy /var/lib/tsuru
run     cp /var/lib/tsuru/buildpack/start /var/lib/tsuru
run     /var/lib/tsuru/buildpack/install
run     chmod +x /var/lib/tsuru/deploy
