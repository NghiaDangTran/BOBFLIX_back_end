# BOBFLIX_back_end

# ~~Signed URL~~ 
Signed Url give us an esay method to stream file but one problem in our case is that we need to read alot of file at once time so that one Signed Url is not enough to do it, we can walk around this by change all of our m3u8 script into a short term signed, but it will slow the time to load it.
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
<br>
set the s3 bucket policy and OAC
![image](https://user-images.githubusercontent.com/33323750/209884997-f951612c-d651-40c8-93c9-245885bfcf18.png)
![image](https://user-images.githubusercontent.com/33323750/209885041-817c2c06-b17e-4ac5-88ba-cae7bef63139.png)

