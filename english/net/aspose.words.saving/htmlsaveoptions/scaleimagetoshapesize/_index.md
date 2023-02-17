---
title: HtmlSaveOptions.ScaleImageToShapeSize
second_title: Aspose.Words for .NET API Reference
description: HtmlSaveOptions property. Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML MHTML or EPUB. Default value is true in C#.
type: docs
weight: 450
url: /net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is `true`.

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

## Remarks

An image in a Microsoft Word document is a shape. The shape has a size and the image has its own size. The sizes are not directly linked. For example, the image can be 1024x786 pixels, but shape that displays this image can be 400x300 points.

In order to display an image in the browser, it must be scaled to the shape size. The `ScaleImageToShapeSize` property controls where the scaling of the image takes place: in Aspose.Words during export to HTML or in the browser when displaying the document.

When `ScaleImageToShapeSize` is `true`, the image is scaled by Aspose.Words using high quality scaling during export to HTML. When `ScaleImageToShapeSize` is `false`, the image is output with its original size and the browser has to scale it.

In general, browsers do quick and poor quality scaling. As a result, you will normally get better display quality in the browser and smaller file size when `ScaleImageToShapeSize` is `true`, but better printing quality and faster conversion when `ScaleImageToShapeSize` is `false`.

In addition to shapes containing individual raster images, this option also affects group shapes consisting of raster images. If `ScaleImageToShapeSize` is `false` and a group shape contains raster images whose intrinsic resolution is higher than the value specified in [`ImageResolution`](../imageresolution/), Aspose.Words will increase rendering resolution for that group. This allows to better preserve quality of grouped high resolution images when saving to HTML.

## Examples

Shows how to disable the scaling of images to their parent shape dimensions when saving to .html.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Insert a shape which contains an image, and then make that shape considerably smaller than the image.
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            Shape imageShape = builder.InsertImage(image);
            imageShape.Width = 50;
            imageShape.Height = 50;

            // Saving a document that contains shapes with images to HTML will create an image file in the local file system
            // for each such shape. The output HTML document will use <image> tags to link to and display these images.
            // When we save the document to HTML, we can pass a SaveOptions object to determine
            // whether to scale all images that are inside shapes to the sizes of their shapes.
            // Setting the "ScaleImageToShapeSize" flag to "true" will shrink every image
            // to the size of the shape that contains it, so that no saved images will be larger than the document requires them to be.
            // Setting the "ScaleImageToShapeSize" flag to "false" will preserve these images' original sizes,
            // which will take up more space in exchange for preserving image quality.
            HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

            doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);

            FileInfo fileInfo = new FileInfo(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.001.png");

#if NET48 || JAVA
        if (scaleImageToShapeSize)
            Assert.That(3000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(20000, Is.LessThan(fileInfo.Length));
#elif NET5_0_OR_GREATER
        if (scaleImageToShapeSize)
            Assert.That(10000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(30000, Is.LessThan(fileInfo.Length));
#endif
```

### See Also

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../htmlsaveoptions/)
* assembly [Aspose.Words](../../../)
