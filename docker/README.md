# Docker

## Docker file
:point_right: When building an image from slim source always make sure the `gcc` and `make` are installed

:point_right: When creating an image use `build --no-cache` when runnig build over and over again to ensure that all the steps will be repeated

---
### Rails
####  Nokogiry
Nokogiry needs folloving libs on Debian like systems

- libxml2-dev
- libxslt-dev
- pkg-config 
