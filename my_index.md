# Compare_Your_Image
## Description

[![](https://avatars.mds.yandex.net/i?id=148223d166e235d7f51ed5a25dd3a583_sr-5680887-images-thumbs&n=13)](https://google.com)

Compare_Your_Image does compare 2 input images Pixel-By-Pixel (the 1st one is represented by the given Image object, the 2nd is specified by the Image parameter), and returns result with differences of set of rectangles.



## Declaration

| Parameters | Specification |
| ------ | ------ |
| Image | An image object or an object that has the Image method, which returns an Image object |
| PixelTolerance | Integer, default value: 0 |
| ColorTolerance | Integer, default value: 0 |

## Parameters

> Image

The Image object that represents the image to be compared with the ImageObj image.

> PixelTolerance

Allows you to skip light differences between the pixels during the algorithm sequence. If the number of different pixels is less than or equal to PixelTolerance, then TestOver thinks the images are to similar to each other.

> ColorTolerance

Lets you ignore differences of 2 images. An acceptable difference for each color component (red, green and blue) of the compared pixels is represented as an integer value within the range 0-255. Two pixels are considered identical if the difference between intensities of each of their color components does not exceed the specified value.

When ColorTolerance is 0 (default value), compared pixels are considered identical only if they have exactly the same color. When ColorTolerance is 255, pixels of any color are considered identical.

## Result Value



## Example
The following code compares two images, which are represented by the Image objects.
```sh
def Test():
  Img1 = Utils.Image
  Img2 = Utils.Image
  Img1.LoadFromFile("D:\\Data\\img1.png")
  Img2.LoadFromFile("D:\\Data\\img2.png")
  # Comparing the images using the Compare method
  if not Img1.Compare(Img2):
    Log.Image(Img1)
    Log.Image(Img2)
  # Comparing the images using the Difference method
  # ResultImage = Img1.Difference(Img2)

```
## Appendix
- 

