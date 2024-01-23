# Configuring Static IP Address in Ubuntu

## Identifying Network Interface

Before proceeding, it's essential to identify the network interface that needs a static IP address. The most common network interface is often named `eth0` or `ens33`. This information can be obtained using the following command:
```bash
ip addr
```

## Editing the Network Configuration File

The primary configuration file for network interfaces in Ubuntu is typically found in the `/etc/netplan/` directory and ends with the .yaml extension.
```bash
sudo vi /etc/netplan/01-network-manager-all.yaml
```

## Adding Static IP Configuration

Within the configuration file, add the necessary details for the static IP address. The following example illustrates the addition of a static IP configuration for the `ens33` interface:
```yaml
network:
  version: 2
  renderer: networkd
  ethernets:
    ens33:
      addresses:
        - <ip address>/<subnet mask>
      gateway4: <gateway address>
      nameservers:
          addresses: <dns address>
```
* `addresses`: Specifies the desired static IP address and subnet mask.
* `gateway4`: Specifies the IP address of the default gateway.
* `nameservers`: Specifies the DNS servers for name resolution.

## Applying Changes

After editing the configuration file, save the changes and apply them using the following command:
```bash
sudo netplan apply
```