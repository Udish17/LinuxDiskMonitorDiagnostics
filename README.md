# LinuxDiskMonitorDiagnostics
This MP adds diagnostics task to the Linux File System Monitor for additional information.

# Pre-Requisites

If you are using a locked down sudoers configuration for the SCOM UNIX/Linux monitoring account, then add the below line to the sudeors file.

*Make sure to change the SCOM UNIX/Linux monitoring account and the system name

*This can be modified with globbing to include all file system

`scxmon ALL=(root) NOPASSWD: /bin/sh -c find /var -type f -exec du -Sh {} + | sort -rh 2> /dev/null | head -n 5`
