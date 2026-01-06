# Linux Live Monitoring Using journalctl

## Objective
To monitor live SSH authentication events on a Linux system using journalctl for security analysis.

## Tool Used
- journalctl
- grep
- OpenSSH

## Monitoring Command
```bash
sudo journalctl -f | grep -i ssh


## Testing Method
ssh fakeuser@<your_IP>
