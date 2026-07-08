[![bluebuild build badge](https://github.com/wegweg7979/hurunagus-silverblue/actions/workflows/build.yml/badge.svg)](https://github.com/wegweg7979/hurunagus-silverblue/actions/workflows/build.yml)

<img width="402" height="426" alt="542900251-a3d3f06c-29eb-40a7-a096-213a3418af8e" src="https://github.com/user-attachments/assets/9fd35c36-06b1-4b77-8160-c663de0a53a9" />







Declarative, Atomic, immutable linux system. Built from atomic fedora, specifically Fedora silverblue, with customisations including the cachyOS kernel (v3 compatible cpus only) pre-installed. SCX schedular BPFland enabled by default. WM Niri, with Dank Material Shell, also Gnome 50 set up how i like it. (Dash to panel, Tiling Shell) Contains *MY* software choices for all types of computing. (These cannot be uninstalled by the user). Dont use this- make your own with bluebuild, it is not too difficult. 

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
- To generate an installer .iso : 
  ```
  sudo bluebuild generate-iso --iso-name hurunagus.iso image ghcr.io/wegweg7979/hurunagus-silverblue
  ```



Obligitory screenshots:
Gnome 50
<img width="1921" height="1080" alt="hurunagus" src="https://github.com/user-attachments/assets/eb67128e-db0f-4b7c-b1b4-a93caeb378d8" />
Niri + Dank Material Shell
<img width="1920" height="1080" alt="hurunagus-niri-dms" src="https://github.com/user-attachments/assets/a2536a9c-bec1-4578-95dd-b535fdc04c1a" />


