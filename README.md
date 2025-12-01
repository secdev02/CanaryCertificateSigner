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

This allows for testing schemes like LDAP:// :) 

Or other shenanigans


Create A Canarytoken - DNS or HTTP

Sample Intereptor Use 

`\Interceptor_AIA_CDP.ps1  -AIAUrl "http://192.168.1.100:8082/i.cer" -CDPUrl "http://192.168.1.100:8082/i.crl"

