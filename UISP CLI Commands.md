# Check if eth cable is plugged in
```bash
ethtool -S eth0
```
Unplugged cable will show all 0's in the output, if plugged in this will show SNR
#### ✓ Cable plugged in:
```bash
NIC statistics:
     SNR for pair 0, dB         : 30
     SNR for pair 1, dB         : 30
     SNR for pair 2, dB         : 30
     SNR for pair 3, dB         : 30
     Cable length,m (+/- 20m)   : 18
```
#### 𐄂 No cable plugged in:
```bash
NIC statistics:
     SNR for pair 0, dB         : 0
     SNR for pair 1, dB         : 0
     SNR for pair 2, dB         : 0
     SNR for pair 3, dB         : 0
     Cable length,m (+/- 20m)   : 0
```


# Check for cable errors

```bash
mca-status | grep Error
```

# Print out status data
```bash
mca-status
```

# Check signal
```bash
mca-status | grep signal
```

# Check firmware
```
mca-status | head -n 1 | awk -F, '{print $3}'
```

# SSH
#ubiquiti #ubiquitissh #ssh #ansible

```bash
#!/bin/bash  
  
#echo "Test script data"  
  
#ssh -i /notpasswords/ubi-ssh-key -o HostKeyAlgorithms=+ssh-rsa -o PubkeyAcceptedKeyTypes=+ssh-rsa admin@10.0.0.29 'm  
ca-status | grep link'  
  
ssh -i /notpasswords/ubi-rsa -o HostKeyAlgorithms=+ssh-rsa -o PubkeyAcceptedKeyTypes=+ssh-rsa admin@10.0.0.29 'mca-st  
atus | grep link'
```
