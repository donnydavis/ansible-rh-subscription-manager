#This is based on a differnet role by Christoph Görn


=============================
  https://galaxy.ansible.com/goern/rh-subscription-manager/

This will configure a Red Hat Enterprise Linux 7 subscription manager, registering
it either to the portal or to a Red Hat Satellite 6.


Requirements
------------
A valid Red Hat subscription.


Role Variables
--------------
rh_username
rh_password
rh_poolid


Dependencies
------------
None


Example Playbook
----------------
- name: Register to RHN
  hosts: webserver
  remote_user: cloud-user
  become: yes
  become_method: sudo
  roles:
     - { role: donnydavis.rh-subscription-manager, rh_username: getyourown, rh_password: nottelling,  rh_poolid: randomstringofnumbersfromredhat, repos: --enable rhel-7-server-rpms }



License
-------
GPLv3


Author Information
------------------
Christoph Görn <goern@redhat.com>
Donny Davis <dondavis@redhat.com>


References
----------
