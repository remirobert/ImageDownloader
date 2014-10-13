<p align="center">
  <h1 align="center">ImageDownloader</h1>
</p>

ImageDownloader allows you to download image from url on asynchronous thread.
All images after download are stored in memory.
The next time the image will be loaded from the disk, it's faster ! Very usefull for a photo app, or social app like Facebook.

ImageDownloader uses **MD5** for store the image according to the url.
For use ImageDownloader, you have to add the following line to your **Bridging Header**:

```Objective-c
#import <CommonCrypto/CommonCrypto.h>
```


<p align="center">
  <h2 align="center">How to use it</h2>
</p>

Use the block completion for get the UIImage and do whatever you want with it.

```Swift
let urlImage = "http://fc01.deviantart.net/fs70/i/2014/284/2/0/raiden_by_keprion-d82epij.jpg"

ImageDownloader.downloadImage(urlImage: urlImage) { (imageDownloaded) -> () in
  imageView.image = imageDownloaded
}
```

You can use a another method for fit the UIImage with a size:

```Swift
ImageDownloader.downloadImageWithSize(urlImage: "http://fc01.deviantart.net/fs70/i/2014/284/2/0/raiden_by_keprion-d82epij.jpg", sizeImage: CGSizeMake(200, 200))
{ (imageDownloaded) -> () in
  imageView.image = imageDownloaded
  imageView.contentMode = UIViewContentMode.ScaleAspectFill
}
```

You can use a UIImageView extension for download a image as well. The image will be displayed on the UIImageView automatically after completion.

```Swift
imageView.downloadImage("http://fc01.deviantart.net/fs70/i/2014/284/2/0/raiden_by_keprion-d82epij.jpg")
```

<h1 align="center">Author</h1>
Rémi ROBERT, remirobert33530@gmail.com

ImageDownloader is available under the MIT license. See the LICENSE file for more info.
