## singularity shell

### syntax

```
$ singularity shell [options] image.sif
```

### blast

Let's go inside the pulled `blast` container.

```
$ singularity shell blast_2.17.0.sif
Singularity> more /etc/os-release
PRETTY_NAME="Ubuntu 22.04.5 LTS"
NAME="Ubuntu"
VERSION_ID="22.04"
VERSION="22.04.5 LTS (Jammy Jellyfish)"
VERSION_CODENAME=jammy
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
```

[Next: Run container](run.md)

[Previous: singularity](pull.md)
