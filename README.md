# debian-installer (d-i) as a service

## Usage

### Debian

 * Download an official Debian [netinst](https://www.debian.org/devel/debian-installer/) image.
 * Visit [the demo site](https://sylee.org/d-i/), edit, and save your
   preseed.cfg and late\_command script.
 * Boot from the netinst image you just downloaded with the following kernel
   parameters.

`auto url=sylee.org`

### Ubuntu

 * Download an official Ubuntu [netboot](http://cdimage.ubuntu.com/netboot/) image.
 * Visit [the demo site](https://sylee.org/d-i/?share=00000000), edit, and
   save your preseed.cfg and late\_command script.
 * Boot from the netboot image you just downloaded with the following kernel
   parameters.

`auto=true url=sylee.org netcfg/get_hostname=ubuntu`

## Setup the service

`pip install flask`

`FLASK_DEBUG=1 FLASK_APP=service.py flask run`
