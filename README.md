Declarative, Atomic, immutable linux system. Built from atomic fedora, specifically a customized silverblue for my use only. Contains highly opinionated software list for all types of computing. ITS JUST SILVERBLUE PLUS SOME APPS

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



