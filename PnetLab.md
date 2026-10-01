## 1.Pnetlab the firewall isn't start :

root@pnetlab:~# `grep -cw vmx /proc/cpuinfo` 
0

actual proxmox -> pnet -> cpu: kvm64 : to change cpu: host -> open proxmox shell 
	 `qm set  101  --cpu host `
	` qm shutdown 101`
	` qm start 101`
root@pnetlab:~# `grep -cw vmx /proc/cpuinfo` 
2
