Showing who's streaming what from my plex and when.
```bash
strace -Tt -o /tmp/tail.trace tail --follow=name Plex\ Media\ Server.log | egrep '\[.{0,3}\].[a-zA-Z ]{0,}\(ID. [0-9]{1,8}\)'
```
Header grabber with netcat
```bash
for f in {80..1024}; do nc -v 127.0.0.1 $f; done 
```

Used to upload screenshot to my server,
```bash
name=$(cat /proc/sys/kernel/random/uuid).jpg;import $name;scp -q $name loot:/var/www/html/loot;echo http://datapor.no/loot/$name | xclip;
```

get the uniq import in .py files, due to people not making requirements.txt files, one have to do this ;_;
```bash
for k in $(grep -r "import" | cut -d' ' -f2 | sort --unique);do pip install  $k;done;
```

other
```bash
wget -qO- https://www.spotify.com/no/download/linux | egrep 'recv-keys\s\w+'
puttygen key.ppk  -O private-openssh -o id_rsa
puttygen key.ppk  -O public-openssh -o id_rsa.pub
boolivar=$1;docker="docker-compose -f docker-compose.yml -f docker-compose.override.yml up --build "; if [ "$boolivar" = True ];then echo $docker"-d";else echo $docker;fi
ffmpeg -i in.mp4 -vn -acodec libmp3lame -ac 2 -ab 160k -ar 48000 out.mp3
```
