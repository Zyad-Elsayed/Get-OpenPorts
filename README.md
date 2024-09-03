# Get-OpenPorts

`Get-OpenPorts` is a PowerShell script designed to scan a given IP address or a list of IP addresses for open ports. The script allows you to specify different sets of ports or provide a custom list, and it saves the results to a file. It also includes functionality to check the reachability of the IP address before performing the port scan.

## Features

- Scan a single IP address or multiple IP addresses from a list.
- Support for predefined port sets (e.g., Top-500, Top-1000) and custom port ranges.
- Results saved to a specified output file.
- Options to measure time elapsed in seconds, minutes, or hours.

## Parameters

- `IP` (String): The single IP address to scan.
- `IPsList` (String): Path to a file containing a list of IP addresses to scan.
- `OutPutFile` (String, default: "OutPut.txt"): Path to the file where results will be saved.
- `Ports` (String): Specify which ports to scan from predefined sets or use 'Custom' for a custom port list.
  - Options: `Top-500`, `Top-1000`, `Top-Nmap`, `Top-5000`, `Top-10000`, `All-Ports`
- `CustomPorts` (String): Custom port ranges or individual ports in the format "port1,port2,..,portN" or "startPort..endPort".
- `Period` (String, default: 'Seconds'): The time period for measuring elapsed time.
  - Options: `Seconds`, `Minutes`, `Hours`

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Zyad-Elsayed/Get-OpenPorts.git
   ```

2. Navigate to the project directory:

   ```bash
   cd Get-OpenPorts
   ```

3. Run the script using PowerShell:

   ```powershell
   .\Get-OpenPorts.ps1
   ```


## Usage

1. **Scan a Single IP Address:**

   ```powershell
   .\Get-OpenPorts.ps1 -IP "192.168.1.1" -Ports "Top-1000" -OutPutFile "results.txt"
   ```

2. **Scan IPs from a List:**

   ```powershell
   .\Get-OpenPorts.ps1 -IPsList "C:\path\to\ips_list.txt" -Ports "Top-500" -OutPutFile "results.txt"
   ```

3. **Custom Port Scan:**

   ```powershell
   .\Get-OpenPorts.ps1 -IP "192.168.1.1" -Ports "Custom" -CustomPorts "22,80,443,1000..2000" -OutPutFile "results.txt"
   ```

4. **Change Time Measurement Period:**

   ```powershell
   .\Get-OpenPorts.ps1 -IP "192.168.1.1" -Ports "Top-500" -Period "Minutes"
   ```

## Contributing

Feel free to submit pull requests or open issues if you find any bugs or have suggestions for improvements.
