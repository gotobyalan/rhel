# Tuning Profiles

- [dnf list tuned]
- [systemctl is-enabled tuned]
systemctl is-active tuned
tuned-adm list
cat /usr/lib/tuned/virtual-guest/tuned.conf

sysctl vm.dirty_ratio -> 30
sysctl vm.swappiness -> 30

cat /usr/lib/tuned/throughput-performance/tuned.conf

vm.dirty_ratio=40
vm.dirty_background_ratio=10

#change active profile
tuned-adm profile throughput-performance
sysctl vm.dirty_ratio -> 40
sysctl vm.swappiness -> 10

