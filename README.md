The `ip addr` command in Linux is used to display IP addresses and network interfaces. Here's a list of common options and how to use them:

1. **List all IP addresses and interfaces:**
   ```sh
   ip addr
   ```
   or
   ```sh
   ip address show
   ```

2. **Show IP address for a specific interface:**
   ```sh
   ip addr show dev <interface_name>
   ```
   For example, to show the IP address for `eth0`:
   ```sh
   ip addr show dev eth0
   ```

3. **Add an IP address to an interface:**
   ```sh
   sudo ip addr add <ip_address>/<prefix_length> dev <interface_name>
   ```
   For example, to add IP address `192.168.1.10` with a prefix length of `24` to `eth0`:
   ```sh
   sudo ip addr add 192.168.1.10/24 dev eth0
   ```

4. **Delete an IP address from an interface:**
   ```sh
   sudo ip addr del <ip_address>/<prefix_length> dev <interface_name>
   ```
   For example, to delete IP address `192.168.1.10` from `eth0`:
   ```sh
   sudo ip addr del 192.168.1.10/24 dev eth0
   ```

5. **Flush all IP addresses from an interface:**
   ```sh
   sudo ip addr flush dev <interface_name>
   ```
   For example, to flush all IP addresses from `eth0`:
   ```sh
   sudo ip addr flush dev eth0
   ```

These commands are useful for managing network configurations directly from the command line.
