<h1 align="center">UNIT3D Community Edition Installer</h1>

<p align="center"><b>NOTE: This only works for a fresh server with nothing on it but a new OS install!</b></p>

## This Repository

Installer for the [UNIT3D-Community-Edition](https://github.com/HDInnovations/UNIT3D).

**Officially Supported OS's**
- Ubuntu 22.04 LTS (Jammy Jellyfish)

**Requirements**
- Meilisearch 1.12+
  Follow step 1 of this [Guide](https://github.com/retro37/UNIT3D-Community-Edition/blob/testing/docs/meilisearch_setup.md)
  

## Installation

**To install UNIT3D run the following:** (and follow the instructions. must have a proper valid domain pointing to your server IP via A RECORD and CNAME for www)
```
sudo apt -y install git
git clone https://github.com/retro37/UNIT3D-Installer.git installer
cd installer
sudo ./install.sh
```

## After Installation

- Follow step 2 and 3.2 of this [Guide](https://github.com/retro37/UNIT3D-Community-Edition/blob/testing/docs/meilisearch_setup.md)


## NOTE
**If you are running UNIT3D on a non HTTPS instance you MUST change the following configs**
```
.env  <-- SESSION_SECURE_COOKIE must be set to false
config/secure-headers.php   <-- HTTP Strict Transport Security must be set to false
config/secure-headers.php   <-- Content Security Policy must be disabled
```
