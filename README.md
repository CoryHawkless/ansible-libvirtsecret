# ansible-libvirtsecret
This is intended to be used an an Ansible role
Used to deploy libvirt secret for allowing libvirt to connect to ceph

Required vars
rbd_secret_uuid
rbd_secret_key

Example to create ceph creds:
ceph auth get-or-create client.openstack -o ceph.client.openstack.keyring
ceph auth caps client.openstack mon 'allow r' osd "allow class-read object_prefix rbd_children, allow rwx pool=volumes, allow rx pool=images"
 
