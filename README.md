# BOBFLIX_back_end


private key: download openssl
<br>
run this command with admin in cmd
```
cd C:\Program Files\Git\usr\bin
openssl.exe
genrsa -out private_key_s3.pem
rsa -pubout -in private_key_s3.pem -out public_key_s3.pem
```
get that public file to cloudFront
