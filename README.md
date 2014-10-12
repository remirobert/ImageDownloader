<p align="center">
  <h1 align="center">ImageDownloader</h1>
</p>

ImageDownloader allows you to download image from url on asynchronous thread.
All images after download are stored in memory.
The next time the image will be loaded from the disk, it's faster ! Very usefull for a photo app, or social app like Facebook.

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
