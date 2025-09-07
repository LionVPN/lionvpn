# How to Clear DNS Cache on Chrome and Windows

DNS cache stores IP addresses of websites you've visited to speed up future connections. However, sometimes you need to clear this cache to resolve connectivity issues or access updated website configurations.

## Clear DNS Cache in Google Chrome
.md
### Method 1: Using Chrome's Internal DNS Tool

1. **Open Chrome** and type the following in the address bar:
   ```
   chrome://net-internals/#dns
   ```

2. Press **Enter** to access the DNS settings page

3. Click the **"Clear host cache"** button

4. You should see "Host resolver cache cleared" message

### Method 2: Using Chrome Flags (Alternative)

1. Type in the address bar:
   ```
   chrome://settings/security
   ```

2. Scroll down to **"Use secure DNS"**

3. Toggle it off and on again to reset DNS settings

### Method 3: Hard Refresh (Quick Fix)

1. Open the website you're having issues with

2. Press:
   - **Windows**: `Ctrl + Shift + R`
   - **Mac**: `Cmd + Shift + R`

## Clear DNS Cache on Windows

### Windows 11/10

#### Method 1: Using Command Prompt

1. **Open Command Prompt as Administrator**:
   - Press `Windows + X`
   - Select "Windows Terminal (Admin)" or "Command Prompt (Admin)"

2. Type the following command and press Enter:
   ```cmd
   ipconfig /flushdns
   ```

3. You should see: "Successfully flushed the DNS Resolver Cache"

#### Method 2: Using PowerShell

1. **Open PowerShell as Administrator**:
   - Right-click Start button
   - Select "Windows PowerShell (Admin)"

2. Run the command:
   ```powershell
   Clear-DnsClientCache
   ```

#### Method 3: Using Run Dialog

1. Press `Windows + R` to open Run dialog

2. Type: `cmd /k ipconfig /flushdns`

3. Press Enter (Command Prompt will open and flush DNS automatically)

### Windows 8/7

1. **Open Command Prompt as Administrator**:
   - Click Start
   - Type "cmd"
   - Right-click "Command Prompt" and select "Run as administrator"

2. Execute:
   ```cmd
   ipconfig /flushdns
   ```

## Additional DNS Commands (Windows)

### View DNS Cache
```cmd
ipconfig /displaydns
```

### Release IP Address
```cmd
ipconfig /release
```

### Renew IP Address
```cmd
ipconfig /renew
```

### Reset Winsock
```cmd
netsh winsock reset
```

### Reset TCP/IP Stack
```cmd
netsh int ip reset
```

## When to Clear DNS Cache

Clear DNS cache when you experience:

- **Website not loading** despite working for others
- **Wrong website version** showing (old site instead of updated one)
- **DNS errors** like "DNS_PROBE_FINISHED_NXDOMAIN"
- **After changing DNS servers** (e.g., switching to Google DNS or Cloudflare)
- **VPN connection issues** where sites don't resolve properly
- **404 errors** on sites you know exist

## Quick Troubleshooting Tips

1. **Clear both Chrome and Windows DNS cache** for best results
2. **Restart your browser** after clearing Chrome's DNS cache
3. **Check your hosts file** at `C:\Windows\System32\drivers\etc\hosts`
4. **Try different DNS servers**:
   - Google: 8.8.8.8, 8.8.4.4
   - Cloudflare: 1.1.1.1, 1.0.0.1
   - OpenDNS: 208.67.222.222, 208.67.220.220

## For Network Administrators

### Flush DNS on Domain Controllers
```powershell
dnscmd /clearcache
```

### Clear DNS on Remote Computers
```powershell
Invoke-Command -ComputerName "PC-Name" -ScriptBlock {Clear-DnsClientCache}
```

## Common Issues and Solutions

### "Access Denied" Error
- Ensure you're running Command Prompt/PowerShell as Administrator
- Disable antivirus temporarily if it blocks the command

### DNS Still Not Resolving
1. Clear browser cache and cookies
2. Reset network adapter:
   ```cmd
   netsh int ip reset
   netsh winsock reset
   ```
3. Restart computer
4. Check firewall settings

### Chrome-Specific Issues
- Clear browsing data: `Ctrl + Shift + Delete`
- Reset Chrome settings: chrome://settings/reset
- Disable extensions that might interfere with DNS

---

**Note**: DNS changes may take a few minutes to propagate. If issues persist, contact your network administrator or ISP.
