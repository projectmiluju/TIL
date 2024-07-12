# 20240713

## ProJect Vinyl

```
iptables -A PREROUTING -t nat -i eth0 -p tcp --dport 80 -j REDIRECT --to-port 8080
```

<img alt="포트포워딩" src="https://github.com/projectmiluju/TIL/blob/main/202407/20240713/portforwarding.png" width="1000"/></img>
