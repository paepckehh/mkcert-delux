# OVERVIEW 

This is just a small (demonstrator/experimental) fork of filippo.io/mkcert.

If upstream is intrested (adding 9 LOCs + some, sight, dependencys)
i would love to prep a small PR and kill this fork.

ORIGINAL SOURCE: [filippo.io/mkcert](https://filippo.io/mkcert)

# WHATS NEW FEATUES??

The delux version does help you to understand what the new certificate 
is and does and allows by provide you a small summary report.

* Just add the usual NO_COLOR=true to env to switch off the color. 
* Just add the usual VERBOSE=true to env to get an full openssl-emulated dump.

The new code is 100% pure golang only, no cgo, NO OPENSSL (CMD) NEEDED! 

* add (minimal/basic) support for FreeBSD rootCA
* add Ed25519 certificates (REMINDER!: still lack of in Chrome)

# INSTALL

```
go install paepcke.de/mkcert-delux@latest
```

### DOWNLOAD (prebuild)

[github.com/paepckehh/mkcert-delux/releases](https://github.com/paepckehh/mkcert-delux/releases)

# SHOWTIME 

``` Shell
mkcert-delux -install
The local CA is now installed in the system trust store! 
X509 Cert Subject           : [CN=mkcert root@rpi2b32-pnoc,OU=root@rpi2b32-pnoc,O=mkcert development CA] 
X509 Cert Status            : [VALID] [for the next 3652 days]
X509 Cert Signature Algo    : [VALID] [SHA256-RSA] 
X509 Cert Public Key        : [VALID] [RSA] [3072] [e:65537]
X509 Cert KeyPin [base64]   : [G48MG3AB/rv8h9DHmASNG5XxIJU9OtBY5868Eiuu4kI=] 
X509 Cert Key Usage         : [CRITICAL] [Certificate Signing] 
X509 CA Authority           : [YES]
X509 CA SelfSigned          : [VALID] [RootCA]
X509 CA Allows SubCAs       : [NO] [PathLen:0]
X509 Issuer Signature By    : [CN=mkcert root@rpi2b32-pnoc,OU=root@rpi2b32-pnoc,O=mkcert development CA] 
```

``` Shell
VERBOSE=true mkcert-delux -install
The local CA is now installed in the system trust store! 
X509 Cert Subject           : [CN=mkcert root@rpi2b32-pnoc,OU=root@rpi2b32-pnoc,O=mkcert development CA] 
X509 Cert Status            : [VALID] [for the next 3652 days]
X509 Cert Signature Algo    : [VALID] [SHA256-RSA] 
X509 Cert Public Key        : [VALID] [RSA] [3072] [e:65537]
X509 Cert KeyPin [base64]   : [G48MG3AB/rv8h9DHmASNG5XxIJU9OtBY5868Eiuu4kI=] 
X509 Cert Key Usage         : [CRITICAL] [Certificate Signing] 
X509 CA Authority           : [YES]
X509 CA SelfSigned          : [VALID] [RootCA]
X509 CA Allows SubCAs       : [NO] [PathLen:0]
X509 Issuer Signature By    : [CN=mkcert root@rpi2b32-pnoc,OU=root@rpi2b32-pnoc,O=mkcert development CA] 
X509 OpenSSL compatible X509 Certificate Decoder Report
Certificate:
    Data:
        Version: 3 (0x2)
        Serial Number: 142684829434173137506466457614972865445 (0x6b58193b57079beb39021bb81783cba5)
    Signature Algorithm: SHA256-RSA
        Issuer: O=mkcert development CA, OU=root@rpi2b32-pnoc, CN=mkcert root@rpi2b32-pnoc
        Validity:
            Not Before: 2022-12-30 17:37:14 +0000 UTC
            Not After : 2032-12-30 17:37:14 +0000 UTC
        Subject: O=mkcert development CA, OU=root@rpi2b32-pnoc, CN=mkcert root@rpi2b32-pnoc
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
                Public Key: (3072 bit)
                Modulus:
                    ce:aa:d8:24:1d:4f:f3:90:72:18:0c:0e:61:e9:ce:
                    85:71:71:57:33:50:27:bc:6f:51:af:87:61:47:59:
                    ab:29:24:20:a2:fe:57:99:65:9a:ac:a7:5e:89:3b:
                    3d:3a:09:26:90:8d:9f:1d:4b:e8:61:a9:7b:3e:51:
                    c2:c0:93:7d:1d:a2:44:6a:27:d5:aa:e7:75:03:bd:
                    b3:36:d4:43:fa:a0:ef:10:18:99:46:20:ad:0b:73:
                    fa:94:20:08:d7:ba:25:be:3f:90:ed:2b:8c:27:0b:
                    50:75:39:ca:15:cd:ef:74:13:9c:93:47:a6:d4:51:
                    30:26:d4:1e:66:89:ed:c5:cf:37:b7:ac:9f:38:55:
                    cc:ee:cd:2f:91:43:77:59:85:07:13:1c:bb:6d:fb:
                    5b:38:bc:af:10:62:b3:c3:71:29:da:6a:d4:c3:45:
                    6b:02:36:aa:21:8a:ca:6a:eb:ab:42:18:1b:35:92:
                    09:b4:c1:ff:fa:88:36:bd:bb:79:f4:31:68:e4:5e:
                    2d:c1:aa:1c:17:54:f9:4c:d0:a7:c9:50:6e:6e:8b:
                    bf:ef:0b:64:e6:0d:06:81:86:63:84:94:c7:c8:65:
                    8d:24:46:d0:83:56:e5:e7:c9:ef:1e:5a:d3:72:93:
                    66:4e:d6:9f:ae:15:ce:1e:0e:b5:49:55:e3:00:b0:
                    73:fa:63:56:bb:ac:ac:18:bb:d8:54:50:87:a2:69:
                    d1:32:ce:41:68:53:cb:2d:2b:8d:ee:e9:df:59:2a:
                    3a:e0:01:bf:d5:37:25:fc:af:9b:a2:02:11:99:16:
                    58:be:5c:67:ed:cb:d0:24:27:91:4b:58:27:b5:aa:
                    e1:21:e7:4a:49:9f:c4:ba:7b:2e:4f:f8:47:04:f8:
                    fb:1b:8e:b4:6e:75:a7:54:88:44:9e:cc:22:ea:2d:
                    43:f3:fe:ae:c1:3a:c6:8b:73:2a:cf:dc:9d:c0:8c:
                    ca:1c:eb:e4:dd:3d:80:45:10:61:a8:b3:62:9b:a5:
                    70:ea:3c:d0:4d:ef:17:e1:69:
                Exponent: 65537 (0x10001)
        X509v3 extensions:
            X509v3 Subject Key Identifier:
                keyid:6f33c416b2f2a63792f8fd6d6700dbc8cd10380d
            X509v3 Key Usage: critical
                Certificate Signing
            X509v3 Basic Constraints: critical
                CA:true, pathlen:0
    Signature Algorithm: SHA256-RSA
         17:0a:27:5e:bb:02:e0:0e:3f:85:5e:49:2f:54:1a:20:2f:1c:
         cc:4b:ce:7f:65:e1:70:bc:a3:2a:f7:61:b4:63:a9:6d:bb:47:
         12:82:ef:c2:56:08:0c:bc:0e:57:84:c8:44:42:32:96:95:28:
         2a:2a:25:ff:62:28:24:24:5c:ab:44:67:0f:4f:ee:a4:0c:17:
         e7:8c:50:7a:ff:71:4c:8a:86:cd:5f:95:84:d1:71:c4:a5:66:
         ce:98:7d:85:e7:c5:c2:d7:49:88:ed:2a:b7:0a:cc:92:48:17:
         f3:3d:fb:c2:69:1f:df:51:0a:31:56:fa:32:6f:a4:28:22:3c:
         98:b4:e5:bb:e0:36:b7:72:bc:70:9f:64:dd:1a:ae:c4:4f:f7:
         51:0e:9e:9b:e5:ec:62:be:38:fe:09:ad:da:30:81:24:f3:86:
         b2:73:a4:58:ac:78:06:a7:a6:85:e7:38:6e:06:4b:46:5f:c7:
         b8:ea:5b:ac:a3:a7:8b:a3:af:3a:38:12:31:4a:26:1c:48:80:
         61:12:96:59:19:f0:00:43:5d:9f:a0:79:b0:60:6e:ed:e5:40:
         6f:fd:f1:6a:b7:d5:2d:82:dd:dd:6b:9f:12:f5:26:20:af:23:
         70:47:ee:a0:e2:ee:bf:01:9a:f1:80:20:04:d5:e3:10:a5:20:
         3f:0a:62:bf:cf:2c:28:9d:5a:f7:53:ea:5c:2e:38:28:e8:13:
         aa:44:2c:97:8a:de:ae:9d:02:68:21:c7:76:19:53:06:a2:87:
         a6:a7:2f:e0:c8:d4:85:13:d2:b2:39:65:d3:4d:12:9d:df:42:
         c0:a0:3b:eb:e6:6c:94:80:8e:42:af:ff:7d:1b:5c:7e:f2:81:
         3f:54:2d:0f:d5:96:6a:95:4a:7b:5d:a5:80:bd:f5:16:87:68:
         ed:84:a2:9e:19:79:81:11:61:a4:b3:ac:b9:71:6b:d9:fa:85:
         ef:53:ac:fe:aa:84:6a:6b:30:0b:b5:74:f0:ab:27:2b:72:da:
         f0:5c:b6:bd:47:aa:
```
