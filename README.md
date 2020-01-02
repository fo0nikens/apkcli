# apkcli

Command line tool gathering information on APKs

## Install

You can install apkcli directly from [pypi](https://pypi.org/project/apkcli/) : `pip install apkcli`

You can also install it from the source code :
```
git clone https://github.com/Te-k/apkcli.git
cd apkcli
pip install .
```

## Plugins

apkcli is a CLI tool with multiple plugins :

```
usage: apk [-h] {cert,strings,manifest,frosting,info,shell,dex} ...

positional arguments:
  {cert,strings,manifest,frosting,info,shell,dex}
                        Plugins
    cert                Show the certificate
    strings             Extract strings from the DEX files
    manifest            Show the manifest
    frosting            Check if Google Play metadata (frosting) is in the APK
    info                Show the certificate
    shell               Launch ipython shell to analyze the APK file
    dex                 Extract the dex files

optional arguments:
  -h, --help            show this help message and exit
```

Example :

```
> apkcli info 1TopSpy.apk
Metadata
================================================================================
MD5:            3018507704917c208762b69e039bdbbf
SHA1:           aebe6e49ca8522cc0e72429028492e099ddf1f44
SHA256:         5e52438f28275dc2a7e83b989e726f86ba53c915b44f126507763850197646f6
Package Name:   com.topspy.system
App:            System Services

Certificate
================================================================================
SHA1:           656CD7890ED79CE8570D1B7156C31958D5AC1606
Serial:         79667C55
Issuer:         C=US/ST=San Jose/L=CA/O=NOVABAY Solutions/OU=HelloSpy LLC/CN=John Nguyen
Subject:        C=US/ST=San Jose/L=CA/O=NOVABAY Solutions/OU=HelloSpy LLC/CN=John Nguyen
Not Before:     Oct 24 09:02:52 2017 UTC
Not After:      Oct 18 09:02:52 2042 UTC

Permissions
================================================================================
android.permission.ACCESS_WIFI_STATE
android.permission.ACCESS_FINE_LOCATION
[SNIP]

Urls
================================================================================
https://goo.gl/NAOOOI.
https://goo.gl/NAOOOI
http://flushdata.1topspy.com
[SNIP]
```

## License

This code is released under MIT license.
