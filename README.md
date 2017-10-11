# kickstart_file
## Kickstart file to install Fedora

# usage
```sh
virt-install \
--name test1 \
--ram 2048 \
--vcpus 2 \
--disk path=/var/lib/libvirt/images/test1.qcow2,bus=virtio,size=20 \
--location http://172.22.26.203/repos/fedora25/ \
--extra-args='ks=http://172.22.26.203/repos/fedora25/ksfiles/ksnew2.cfg ksdevice=ens3 ip=192.168.124.160 netmask=255.255.255.0 gateway=192.168.124.1 dns=8.8.8.8' \
--network bridge:virbr0
```
