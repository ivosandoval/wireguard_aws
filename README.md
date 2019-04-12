# Install and use AWS-based Wireguard
Scripts automate the installation and use AWS-based Wireguard

## How use

### Installation
```
git clone https://github.com/pprometey/wireguard_aws.git wireguard_aws
cd wireguard_aws
chmod +x initial.sh
./initial.sh
```

The `initial.sh` script removes the previous Wireguard installation (if any) using the `remove.sh` script. It then installs and configures the Wireguard service using the `install.sh` script. And then creates a client using the `add-client.sh` script.

### Add new customer
`add-client.sh` - Script to add a new VPN client. As a result of the execution, it creates a configuration file ($CLIENT_NAME.conf) on the path ./clients/$CLIENT_NAME/, displays a QR code with the configuration, writes a QR code as an image into the .png file ($CLIENT_NAME.png).

```
./add-client.sh
#OR
./add-client.sh $CLIENT_NAME
```

### Reset customers
reset.sh - script that removes information about clients. And stopping the VPN server Winguard
```
./reset.sh
```

### Delete Wireguard
```
./remove.sh
```
