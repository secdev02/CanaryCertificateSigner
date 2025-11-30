# CanaryCertificateSigner
A PowerShell Based Certificate Creation and Signing - for things like EXE and RDP etc...

I wanted more fine tuned control over some certificate properties 

```
. .\CertificateGenerator.ps1

New-SignedExecutable -TokenUrl "http://your-server.com/alert"

```

This allows you to create a custom signed EXE 

```
New-SignedExecutable `
    -TokenUrl "http://default.com" `
    -CDPUrl "http://crl.example.com/mycrl.crl" `
    -AIAUrl "http://aia.example.com/myca.crt"

```

This allows for testing schemes like LDAP:/// :) 

Or other shenanigans


