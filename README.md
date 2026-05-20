[![bluebuild build badge](https://github.com/wegweg7979/hurunagus-silverblue/actions/workflows/build.yml/badge.svg)](https://github.com/wegweg7979/hurunagus-silverblue/actions/workflows/build.yml)

<img width="402" height="426" alt="542900251-a3d3f06c-29eb-40a7-a096-213a3418af8e" src="https://github.com/user-attachments/assets/9fd35c36-06b1-4b77-8160-c663de0a53a9" />
<img width="1921" height="1080" alt="hurunagus" src="https://github.com/user-attachments/assets/aba16fbc-c86e-453a-871c-2423a4c38f21" />



Declarative, Atomic, immutable linux system. Built from atomic fedora, specifically a customized silverblue, with the cachyOS kernel (v3 compatible cpus only) pre-installed. SCX schedular BPFland enabled by default. Contains *MY* software choices for all types of computing. 

To rebase an existing atomic Fedora installation to the latest build:

- First rebase to the unsigned image, to get the proper signing keys and policies installed:
  ```
  rpm-ostree rebase ostree-unverified-registry:ghcr.io/wegweg7979/hurunagus-silverblue:latest
  ```
- Reboot to complete the rebase:
  ```
  systemctl reboot
  ```
- Then rebase to the signed image, like so:
  ```
  rpm-ostree rebase ostree-image-signed:docker://ghcr.io/wegweg7979/hurunagus-silverblue:latest
  ```
- Reboot again to complete the installation
  ```
  systemctl reboot
  ```
- To install on any system, generate an installer .iso : 
  ```
  sudo bluebuild generate-iso --iso-name hurunagus.iso image ghcr.io/wegweg7979/hurunagus-silverblue
  ```
To install the same system without the cachyOS kernel and scx scheduler use:  hurunagus-silverblue2:latest 


