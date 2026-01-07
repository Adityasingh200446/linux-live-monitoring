# Commands Used in Live Monitoring

## Live SSH Monitoring

sudo journalctl -f | grep -i ssh


# When Someone Unauthorized Try To Get Inside Then Attacker System IP Will Show And You Can Block Them Using 

## Detection and Blocking (Simulated)

Failed SSH Login Attempts Were Detected Using:

sudo journalctl | grep -i "Failed password" | awk '{print $(NF-3)}'


#Simulated Blocking of Attacker IP
#Here Replce Attacker IP With The IP You Detcted
sudo iptables -A INPUT -s <attacker-ip> -j DROP


#For Checking Blocked IPs

sudo iptables -L -n


