# prac-ansible-isu-templete

```
# mysql
mysql -u isuconp -pisuconp isuconp

# pprof
sudo go tool trace -http=localhost:1080 /tmp/trace.out

# ssh port foward
ssh -fN -L 0.0.0.0:19999:localhost:19999 x.x.x.x  # netdata
ssh -fN -L 0.0.0.0:1080:localhost:1080 x.x.x.x  # pprof
ssh -fN -L 0.0.0.0:3306:localhost:3306 x.x.x.x  # mysql
ssh -fN -L 0.0.0.0:8080:localhost:8080 x.x.x.x  # grafana
ssh -fN -L 0.0.0.0:9100:localhost:9100 x.x.x.x  # node_exporter
ssh -fN -L 0.0.0.0:3100:localhost:3100 x.x.x.x  # fluent-bit
ps aux | grep ssh

# wipe ps
kill $(ps aux | grep 'ssh -fN -L 0.0.0.0:19999:localhost:19999 x.x.x.x' | grep -v grep | awk '{print $2}')
kill $(ps aux | grep 'ssh -fN -L 0.0.0.0:1080:localhost:1080 x.x.x.x' | grep -v grep | awk '{print $2}')
kill $(ps aux | grep 'ssh -fN -L 0.0.0.0:3306:localhost:3306 x.x.x.x' | grep -v grep | awk '{print $2}')
ps aux | grep ssh
```