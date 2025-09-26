# Task 4: Setup and Use a Firewall on Windows/Linux

## Objective
Configure and test basic firewall rules to allow or block traffic.

## Tools
- Windows Firewall
- UFW (Uncomplicated Firewall) on Linux

## Deliverables
- Screenshot/configuration file showing firewall rules applied.

## Hints/Mini Guide

1. **Open firewall configuration tool**  
   - Windows: Use Windows Firewall via Control Panel or search "Windows Defender Firewall".
   - Linux: Open terminal and use UFW commands.

2. **List current firewall rules**  
   - Windows: View inbound/outbound rules in Firewall settings.
   - Linux:  
     ```bash
     sudo ufw status numbered
     ```

3. **Add a rule to block inbound traffic on a specific port (e.g., 23 for Telnet)**  
   - Windows: Add a new inbound rule for TCP port 23, set action to "Block".
   - Linux:  
     ```bash
     sudo ufw deny 23/tcp
     ```

4. **Test the rule by attempting to connect to that port locally or remotely**  
   - Use Telnet client or `nc` to check if the port is blocked.

5. **Add rule to allow SSH (port 22) if on Linux**  
   - Linux:  
     ```bash
     sudo ufw allow 22/tcp
     ```

6. **Remove the test block rule to restore original state**  
   - Windows: Delete the inbound rule for port 23.
   - Linux:  
     ```bash
     sudo ufw delete deny 23/tcp
     ```

7. **Document commands or GUI steps used**  
   - Save screenshots or command history.

8. **Summarize how firewall filters traffic**  
   - Firewalls filter traffic by allowing or denying packets based on rules for ports, protocols, and IP addresses. This controls access and protects the system from unauthorized connections.

---

**Example UFW Command Sequence**
```bash
sudo ufw status numbered
sudo ufw deny 23/tcp
sudo ufw allow 22/tcp
sudo ufw delete deny 23/tcp
```

**Example Windows Firewall Steps**
- Open Windows Defender Firewall.
- Go to Advanced Settings.
- Add a new inbound rule for TCP port 23, set Action to "Block".
- Test connection.
- Delete the rule to restore original state.