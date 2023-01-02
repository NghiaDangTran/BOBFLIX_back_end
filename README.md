# BOBFLIX_back_end

# Solution to stream video with Signed Cookie

After more than a week research and many stack overflow post I finaaly found a way to stream file safe and reliable with cloud front ![Using signed cookies
](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-signed-cookies.html) this post will show a basic meaning of what we need to do. Sound easy right, but they didn't say that you can't send cookie CORS when you dont own the domain, so I follow this first ![four step](https://stackoverflow.com/questions/64166589/stream-aws-s3-hls-videos-in-ios-browsers/64988224#64988224) and with additional cloudfront setting




https://stackoverflow.com/questions/64166589/stream-aws-s3-hls-videos-in-ios-browsers/64988224#64988224


# ~~Signed URL~~ 
Signed Url give us an esay method to stream file but one problem in our case is that we need to read alot of file at once time so that one Signed Url is not enough to do it, we can walk around this by change all of our m3u8 script into a short term signed, but it will slow the time to load it.
<br>
~~download openssl~~
<br>
~~run this command with admin in cmd~~
```
cd C:\Program Files\Git\usr\bin
openssl.exe
genrsa -out private_key_s3.pem
rsa -pubout -in private_key_s3.pem -out public_key_s3.pem
```
~~get that public file to cloudFront~~
<br>
~~set the s3 bucket policy and OAC~~
![image](https://user-images.githubusercontent.com/33323750/209884997-f951612c-d651-40c8-93c9-245885bfcf18.png)
![image](https://user-images.githubusercontent.com/33323750/209885041-817c2c06-b17e-4ac5-88ba-cae7bef63139.png)
