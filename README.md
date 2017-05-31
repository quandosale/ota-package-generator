# ota-package-generator
Before running script, install packages via pip
> `pip install -r requirements.txt`

Generate keyfile
> `python __main__.py keys generate firmware/1.pem`

Make package from firmware with keyfile
> `python __main__.py pkg generate --hw-version 52 --sd-req 0x98,0xCAFE --application-version 1 --application firmware/1.hex --key-file firmware/1.pem firmware/1.zip`

Build to standalone executable

> `python setup.py py2exe`