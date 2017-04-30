matthijsbos.vivado
=========

Ansible role for the installation of Xilinx Vivado on Ubuntu.

Requirements
------------
The installer archive for the desired Vivado edition is to be present on the system. Lab editions have OS-specific installer archives. WebPack editions require the "All OS installer Single-File Download". Xilinx installer archives can't be automatically downloaded, since US export regulations require users to be registered and authenticated in order to access the [Xilinx website downloads section](https://www.xilinx.com/support/download.html).

WebPack edition installer archives verified working:
- [Vivado HLx 2017.1: All OS installer Single-File Download](https://www.xilinx.com/member/forms/download/xef.html?filename=Xilinx_Vivado_SDK_2017.1_0415_1.tar.gz&akdm=1) (TAR/GZIP - 20.21 GB) MD5 SUM Value: ee351905f061e19751999e69b41f4b22

Lab edition installer archives verified working:
- [Vivado 2017.1: Lab Edition - Linux](https://www.xilinx.com/member/forms/download/xef.html?filename=Xilinx_Vivado_Lab_Lin_2017.1_0415_1.tar.gz&akdm=1) (TAR/GZIP - 508.01 MB) MD5 SUM Value: 8abe546292f30631325a91699a83df7f

Role Variables
--------------

TODO:
A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - role: matthijsbos.vivado
       vivado_installer_archive_path: ~/Downloads/Xilinx_Vivado_Lab_Lin_2017.1_0415_1.tar.gz
       vivado_version: 2017.1
       vivado_edition: lab
       vivado_location: /home/vagrant/Xilinx
       vivado_headless: true
       vivado_source_bashrc: true
 ```
License
-------

Apache License 2.0

