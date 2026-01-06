
Paste:

```md
# Commands Used in Live Monitoring

## Live SSH Monitoring
```bash
sudo journalctl -f | grep -i ssh


# when someone unauthorized try to get inside ites system IP will show and you can block them using 

## Detection and Blocking (Simulated)

Failed SSH login attempts were detected using:

```bash
sudo journalctl | grep -i "Failed password" | awk '{print $(NF-3)}'


#Simulated Blocking of Attacker IP
#here replce attacker with the IP you Detcted
sudo iptables -A INPUT -s <attacker-ip> -j DROP


#for checking Blocked IPs

sudo iptables -L -n


