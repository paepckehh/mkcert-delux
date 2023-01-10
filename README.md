# OVERVIEW 

This is just a small (demonstrator/experimental) temporary fork of filippo.io/mkcert.

If upstream is intrested (adding 9 LOCs + some, sight, dependencys)
i would love to prep a small PR and kill this fork.

# ORIGINAL SOURCE: [filippo.io/mkcert](https://filippo.io/mkcert/)

# WHATS NEW?

The delux version does help you to understand what the new certificate 
is and does and allows by provide you a small summary report.

* Just add the usual NO_COLOR=true to env to switch off the color. 
* Just add the usual VERBOSE=true to env to get an full openssl-emulated dump.

The new code is 100% pure golang only, no cgo, NO OPENSSL (CMD) NEEDED! 

# ANYTHING ELSE NEW?

* add (minimal/basic) support for FreeBSD rootCA (PR open [#491](https://github.com/FiloSottile/mkcert/pull/491))
* add Ed25519 certificates support 
* Ed25519 REMINDER: still lack of support in Chrome
* Ed25519: reduce embedded sys keygen time from minutes (rsa3072) to less < 1 sec
   

# INSTALL

```
go install paepcke.de/mkcert-delux@latest
```

### DOWNLOAD (prebuild)

[github.com/paepckehh/mkcert-delux/releases](https://github.com/paepckehh/mkcert-delux/releases)

# SHOWTIME 

``` Shell
mkcert-delux -install
Created a new local CA 💥
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
mkcert-delux -install
Created a new local CA 💥
The local CA is now installed in the system trust store! ⚡️
X509 Cert Subject           : [CN=mkcert root@rpi2b32-pnoc,OU=root@rpi2b32-pnoc,O=mkcert development CA] 
X509 Cert Status            : [VALID] [for the next 3652 days]
X509 Cert Signature Algo    : [VALID] [SHA256-RSA] 
X509 Cert Public Key        : [VALID] [RSA] [3072] [e:65537]
X509 Cert KeyPin [base64]   : [L0P3FQrLRZsXdrUnPwTW4FCw0iSmsc9AsUo4zslZLRg=] 
X509 Cert Key Usage         : [CRITICAL] [Certificate Signing] 
X509 CA Authority           : [YES]
X509 CA SelfSigned          : [VALID] [RootCA]
X509 CA Allows SubCAs       : [NO] [PathLen:0]
X509 Issuer Signature By    : [CN=mkcert root@rpi2b32-pnoc,OU=root@rpi2b32-pnoc,O=mkcert development CA] 
X509 Issuer Signature State : [FAIL] [x509: certificate signed by unknown authority (possibly because of "x509: signat] 
X509 OpenSSL compatible X509 Certificate Decoder Report
Certificate:
    Data:
        Version: 3 (0x2)
        Serial Number: 296533402497389686237515087605223637709 (0xdf16418528604ea2a5452d7dbee3c2cd)
    Signature Algorithm: SHA256-RSA
        Issuer: O=mkcert development CA, OU=root@rpi2b32-pnoc, CN=mkcert root@rpi2b32-pnoc
        Validity:
            Not Before: 2022-12-31 08:53:19 +0000 UTC
            Not After : 2032-12-31 08:53:19 +0000 UTC
        Subject: O=mkcert development CA, OU=root@rpi2b32-pnoc, CN=mkcert root@rpi2b32-pnoc
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
                Public Key: (3072 bit)
                Modulus:
                    be:55:56:a9:f4:c3:72:98:e5:1c:7c:89:b5:bc:e4:
                    64:b7:bd:16:a2:9d:c2:06:09:98:67:6b:98:7f:8c:
                    6d:42:18:1c:9e:f9:5b:11:5c:70:7a:96:0c:dd:4a:
                    5f:b7:28:9f:45:92:50:01:e3:3a:12:cd:c2:c3:d7:
                    48:7e:12:8b:47:87:3e:99:3a:b5:bc:2d:a4:c7:44:
                    34:6e:66:a4:31:95:7b:b4:03:56:f0:66:b3:6c:a3:
                    45:37:63:76:30:6a:ee:84:bd:90:04:8c:6a:76:80:
                    38:03:63:42:a4:a1:a6:39:58:df:24:d0:b5:82:06:
                    ac:bb:8e:fb:dd:c2:e5:3b:95:b5:61:11:ea:ec:ff:
                    86:b5:cf:a8:79:ff:90:53:0f:0d:72:01:92:2d:ba:
                    dc:b8:4c:f5:88:76:52:13:1f:4a:22:c4:bf:85:c5:
                    8f:79:e5:b0:35:33:df:ad:79:e9:aa:79:18:4c:15:
                    30:a4:00:5c:2b:e7:d1:e2:ee:68:2a:59:1b:2a:39:
                    db:cf:8f:69:37:33:09:dc:d8:48:1c:80:a7:b6:ce:
                    67:c9:ea:9e:ea:66:e2:41:d4:49:23:32:13:fb:a9:
                    8e:ce:95:13:9a:59:cb:fc:63:6f:92:09:da:32:21:
                    89:82:ad:ec:85:57:31:d5:61:bc:10:62:56:82:a1:
                    8d:b2:de:2b:82:8a:f7:d1:3a:48:bd:06:4e:4a:00:
                    e4:51:0e:44:d0:9e:40:5b:25:81:3a:37:c2:d5:89:
                    33:11:32:0c:49:3d:ab:0d:02:bc:bc:0f:75:30:1b:
                    5e:5c:be:4d:8e:cb:12:1c:ec:d7:77:9a:d2:d6:6b:
                    f9:30:cf:c9:34:d1:f9:41:be:01:93:58:e4:2d:eb:
                    37:2c:40:58:92:fc:3f:ba:cb:4a:3d:d1:df:97:4d:
                    c3:0e:7b:e6:23:fb:e6:cc:6d:80:df:96:19:44:93:
                    27:01:96:6e:9b:a7:1c:2c:6c:25:12:9c:99:4a:47:
                    17:9a:84:8c:b2:4e:5d:94:3d:
                Exponent: 65537 (0x10001)
        X509v3 extensions:
            X509v3 Subject Key Identifier:
                keyid:483d533d246677661ced642d04de98e4ac1d6e66
            X509v3 Key Usage: critical
                Certificate Signing
            X509v3 Basic Constraints: critical
                CA:true, pathlen:0
    Signature Algorithm: SHA256-RSA
         60:37:8a:a7:dc:58:5e:2e:a6:c7:30:a6:52:9e:87:e2:ca:39:
         0a:14:ba:ad:2c:c8:44:7c:4c:d9:e1:ed:00:d8:d9:6c:d1:92:
         30:05:22:d7:18:de:67:59:67:69:b7:34:87:c9:f7:43:e4:8e:
         fa:fa:e2:d0:6f:82:ed:db:58:eb:4b:a8:0d:96:38:a5:18:05:
         2a:f7:60:33:90:89:2d:19:62:0e:0a:11:89:96:fa:38:20:d2:
         b9:df:27:62:f4:6d:02:ac:4a:32:7d:0c:54:fc:95:1f:22:cb:
         d0:e2:95:fa:ba:2a:09:a8:04:1a:be:b5:c7:a9:34:4a:eb:91:
         fd:f7:cb:f0:4c:37:39:2d:13:8e:c7:de:01:56:e4:02:b3:01:
         e3:41:ab:e3:b4:e1:d9:00:28:72:bf:55:7a:26:f4:0f:5c:e9:
         e3:d8:25:95:fc:27:9e:29:33:0d:bc:0c:0d:dc:c1:8a:ce:f3:
         5f:9b:75:4c:bc:5d:9d:4b:e6:de:1d:ef:2f:ed:a0:ae:bf:fb:
         37:23:b8:84:8e:b4:d7:e6:bd:0a:b0:de:30:c9:83:e9:4e:95:
         09:cb:19:48:09:d5:5a:62:10:dc:98:26:d5:47:8a:6a:01:55:
         28:d8:3e:c2:fc:25:2a:0d:35:a4:29:bd:21:2f:c8:c6:91:f8:
         cf:18:4c:a4:ed:f8:fc:b6:48:37:cb:86:09:54:61:48:21:3d:
         bb:69:f1:ca:52:f8:9c:52:12:96:ac:bf:87:b3:75:49:2f:57:
         45:64:9e:98:7b:02:ae:36:b7:f6:22:23:a8:47:b9:2b:cb:f4:
         2b:1a:19:57:b3:df:df:2b:1d:c9:6f:5d:9a:3b:15:09:91:45:
         6d:e2:8d:de:50:9c:eb:38:f6:30:d2:29:a8:a1:f7:c2:9f:8c:
         82:57:dc:de:9e:52:a3:4b:ad:81:ae:35:76:14:0b:1d:14:d1:
         7e:73:10:f0:19:89:51:37:0d:26:1a:c4:6c:6f:cc:64:01:45:
         0a:86:74:1e:fe:b7:
```

# DOCS

[pkg.go.dev/paepcke.de/mkcert-delux](https://pkg.go.dev/paepcke.de/mkcert-delux)

# CONTRIBUTION

Yes, Please! PRs Welcome! 
