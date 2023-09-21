# Setup the base station PC
1. Join the Unitree_GO wifi, password is 888888888.
2. Set the ip address to 192.168.12.170.
3. add IP routes:
```
sudo route add -net 192.168.123.0 netmask 255.255.255.0 gw 192.168.12.1
```
4. Now the PC should be able to communicate with the Head Nano on Unitree. Test the connection:
```
ping 192.168.123.15
```

# Start Unitree Go1
1. Start a new terminal, SSH into the Head Nano:
```
ssh unitree@192.168.123.15
```
2. Setup the environment:
```
source rossetup_head.sh
```
3. Launch the Unitree nodes:
```
roslaunch ice9_unitree unitree.launch
```
4. Repeat Steps 1 and 2, then launch the GPS nodes:
```
roslaunch emlid_reach_ros reach_ros.launch polling_rate:=20
```
