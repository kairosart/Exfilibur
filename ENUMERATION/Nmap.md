## Simple enumeration

```
nmap -A 10.10.17.73 -Pn
```

![[Screenshot from 2025-09-11 10-25-03.png]]

## Deeper enumeration

```
sudo nmap -p- -sS -T4 -v 10.10.17.73 -Pn
```

![[Screenshot from 2025-09-11 10-51-43.png]]

There are only 2 ports opened: 

80/tcp      open  http
3389/tcp open  ms-wbt-server. (-The service running on that port is **ms-wbt-server**, which refers to Microsoft's Remote Desktop Protocol RDP)

**Next step:** [[Gobuster]]