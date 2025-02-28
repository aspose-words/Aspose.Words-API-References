---
title: Watermark.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words for .NET
description: Enhance your documents with the Watermark SetImage method. Effortlessly add stunning image watermarks for a professional touch.
type: docs
weight: 30
url: /net/aspose.words/watermark/setimage/
---
## SetImage(*Image*) {#setimage}

Adds Image watermark into the document.

```csharp
public void SetImage(Image image)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | Image | Image that is displayed as a watermark. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | Throws when the image is `null`. |

## Examples

Shows how to create a watermark from an image in the local file system.

```csharp
Document doc = new Document();

            // Modify the image watermark's appearance with an ImageWatermarkOptions object,
            // then pass it while creating a watermark from an image file.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // We have a different options to insert image:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### See Also

* class [Watermark](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## SetImage(*Image, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_1}

Adds Image watermark into the document.

```csharp
public void SetImage(Image image, ImageWatermarkOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | Image | Image that is displayed as a watermark. |
| options | ImageWatermarkOptions | Defines additional options for the image watermark. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | Throws when the image is `null`. |

## Remarks

If [`ImageWatermarkOptions`](../../imagewatermarkoptions/) is `null`, the watermark will be set with default options.

## Examples

Shows how to create a watermark from an image in the local file system.

```csharp
Document doc = new Document();

            // Modify the image watermark's appearance with an ImageWatermarkOptions object,
            // then pass it while creating a watermark from an image file.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // We have a different options to insert image:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### See Also

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## SetImage(*string, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_2}

Adds Image watermark into the document.

```csharp
public void SetImage(string imagePath, ImageWatermarkOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| imagePath | String | Path to the image file that is displayed as a watermark. |
| options | ImageWatermarkOptions | Defines additional options for the image watermark. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | Throws when the path is `null`. |

## Remarks

If [`ImageWatermarkOptions`](../../imagewatermarkoptions/) is `null`, the watermark will be set with default options.

## Examples

Shows how to create a watermark from an image in the local file system.

```csharp
Document doc = new Document();

            // Modify the image watermark's appearance with an ImageWatermarkOptions object,
            // then pass it while creating a watermark from an image file.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // We have a different options to insert image:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### See Also

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
