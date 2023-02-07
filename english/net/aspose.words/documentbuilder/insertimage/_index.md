---
title: DocumentBuilder.InsertImage
second_title: Aspose.Words for .NET API Reference
description: Inserts an image from a .NET Image object into the document. The image is inserted inline and at 100 scale in C#
type: docs
weight: 370
url: /net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(Image) {#insertimage_3}

Inserts an image from a .NET Image object into the document. The image is inserted inline and at 100% scale.

```csharp
public Shape InsertImage(Image image)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | Image | The image to insert into the document. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples

Shows how to insert an image from an object into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// Below are three ways of inserting an image from an Image object instance.
// 1 -  Inline shape with a default size based on the image's original dimensions:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 -  Inline shape with custom dimensions:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 -  Floating shape with custom dimensions:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## InsertImage(string) {#insertimage_9}

Inserts an image from a file or URL into the document. The image is inserted inline and at 100% scale.

```csharp
public Shape InsertImage(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The file with the image. Can be any valid local or remote URI. |

### Return Value

The image node that was just inserted.

## Remarks

This overload will automatically download the image before inserting into the document if you specify a remote URI.

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples

Shows how to insert gif image to the document.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// We can insert gif image using path or bytes array.
// It works only if DocumentBuilder optimized to Word version 2010 or higher.
// Note, that access to the image bytes causes conversion Gif to Png.
Shape gifImage = builder.InsertImage(ImageDir + "Graphics Interchange Format.gif");

gifImage = builder.InsertImage(File.ReadAllBytes(ImageDir + "Graphics Interchange Format.gif"));

builder.Document.Save(ArtifactsDir + "InsertGif.docx");
```

Shows how to insert a shape with an image into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two locations where the document builder's "InsertShape" method
// can source the image that the shape will display.
// 1 -  Pass a local file system filename of an image file:
builder.Write("Image from local file: ");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.Writeln();

// 2 -  Pass a URL which points to an image.
builder.Write("Image from a URL: ");
builder.InsertImage(ImageUrl);
builder.Writeln();

doc.Save(ArtifactsDir + "Image.FromUrl.docx");
```

Shows how to insert a floating image to the center of a page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Shows how to determine which image will be inserted.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Scalable Vector Graphics.svg");

// Aspose.Words insert SVG image to the document as PNG with svgBlip extension
// that contains the original vector SVG image representation.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words insert SVG image to the document as PNG, just like Microsoft Word does for old format.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);

// Aspose.Words insert SVG image to the document as EMF metafile to keep the image in vector representation.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
```

Shows how to insert an image from the local file system into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are three ways of inserting an image from a local system filename.
// 1 -  Inline shape with a default size based on the image's original dimensions:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 -  Inline shape with custom dimensions:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 -  Floating shape with custom dimensions:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## InsertImage(Stream) {#insertimage_6}

Inserts an image from a stream into the document. The image is inserted inline and at 100% scale.

```csharp
public Shape InsertImage(Stream stream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | The stream that contains the image. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples

Shows how to insert a shape with an image from a stream into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    builder.Write("Image from stream: ");
    builder.InsertImage(stream);
}

doc.Save(ArtifactsDir + "Image.FromStream.docx");
```

Shows how to insert an image from a stream into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Below are three ways of inserting an image from a stream.
    // 1 -  Inline shape with a default size based on the image's original dimensions:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 -  Inline shape with custom dimensions:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 -  Floating shape with custom dimensions:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## InsertImage(byte[]) {#insertimage}

Inserts an image from a byte array into the document. The image is inserted inline and at 100% scale.

```csharp
public Shape InsertImage(byte[] imageBytes)
```

| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | Byte[] | The byte array that contains the image. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples

Shows how to insert an image from a byte array into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // Below are three ways of inserting an image from a byte array.
    // 1 -  Inline shape with a default size based on the image's original dimensions:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 -  Inline shape with custom dimensions:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 -  Floating shape with custom dimensions:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Shows how to insert an image from a byte array into a document (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Decoding the image will convert it to the .png format.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Below are three ways of inserting an image from a byte array.
            // 1 -  Inline shape with a default size based on the image's original dimensions:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 -  Inline shape with custom dimensions:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 -  Floating shape with custom dimensions:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## InsertImage(Image, double, double) {#insertimage_5}

Inserts an inline image from a .NET Image object into the document and scales it to the specified size.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | Image | The image to insert into the document. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples

Shows how to insert an image from an object into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// Below are three ways of inserting an image from an Image object instance.
// 1 -  Inline shape with a default size based on the image's original dimensions:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 -  Inline shape with custom dimensions:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 -  Floating shape with custom dimensions:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

Shows how to insert an image from an object into a document (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Decoding the image will convert it to the .png format.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // Below are three ways of inserting an image from an Image object instance.
    // 1 -  Inline shape with a default size based on the image's original dimensions:
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 -  Inline shape with custom dimensions:
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 -  Floating shape with custom dimensions:
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## InsertImage(string, double, double) {#insertimage_11}

Inserts an inline image from a file or URL into the document and scales it to the specified size.

```csharp
public Shape InsertImage(string fileName, double width, double height)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The file that contains the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples

Shows how to insert an image from the local file system into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are three ways of inserting an image from a local system filename.
// 1 -  Inline shape with a default size based on the image's original dimensions:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 -  Inline shape with custom dimensions:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 -  Floating shape with custom dimensions:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## InsertImage(Stream, double, double) {#insertimage_8}

Inserts an inline image from a stream into the document and scales it to the specified size.

```csharp
public Shape InsertImage(Stream stream, double width, double height)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | The stream that contains the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples

Shows how to insert an image from a stream into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Below are three ways of inserting an image from a stream.
    // 1 -  Inline shape with a default size based on the image's original dimensions:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 -  Inline shape with custom dimensions:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 -  Floating shape with custom dimensions:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## InsertImage(byte[], double, double) {#insertimage_2}

Inserts an inline image from a byte array into the document and scales it to the specified size.

```csharp
public Shape InsertImage(byte[] imageBytes, double width, double height)
```

| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | Byte[] | The byte array that contains the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples

Shows how to insert an image from a byte array into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // Below are three ways of inserting an image from a byte array.
    // 1 -  Inline shape with a default size based on the image's original dimensions:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 -  Inline shape with custom dimensions:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 -  Floating shape with custom dimensions:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Shows how to insert an image from a byte array into a document (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Decoding the image will convert it to the .png format.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Below are three ways of inserting an image from a byte array.
            // 1 -  Inline shape with a default size based on the image's original dimensions:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 -  Inline shape with custom dimensions:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 -  Floating shape with custom dimensions:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## InsertImage(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_4}

Inserts an image from a .NET Image object at the specified position and size.

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | Image | The image to insert into the document. |
| horzPos | RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | Double | Distance in points from the origin to the left side of the image. |
| vertPos | RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | Double | Distance in points from the origin to the top side of the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | WrapType | Specifies how to wrap text around the image. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples

Shows how to insert an image from an object into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// Below are three ways of inserting an image from an Image object instance.
// 1 -  Inline shape with a default size based on the image's original dimensions:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 -  Inline shape with custom dimensions:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 -  Floating shape with custom dimensions:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

Shows how to insert an image from an object into a document (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Decoding the image will convert it to the .png format.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // Below are three ways of inserting an image from an Image object instance.
    // 1 -  Inline shape with a default size based on the image's original dimensions:
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 -  Inline shape with custom dimensions:
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 -  Floating shape with custom dimensions:
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## InsertImage(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_10}

Inserts an image from a file or URL at the specified position and size.

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The file that contains the image. |
| horzPos | RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | Double | Distance in points from the origin to the left side of the image. |
| vertPos | RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | Double | Distance in points from the origin to the top side of the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | WrapType | Specifies how to wrap text around the image. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples

Shows how to insert an image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// There are two ways of using a document builder to source an image and then insert it as a floating shape.
// 1 -  From a file in the local file system:
builder.InsertImage(ImageDir + "Transparent background logo.png", RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 0, 200, 200, WrapType.Square);

// 2 -  From a URL:
builder.InsertImage(ImageUrl, RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 250, 200, 200, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

Shows how to insert an image from the local file system into a document while preserving its dimensions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// The InsertImage method creates a floating shape with the passed image in its image data.
// We can specify the dimensions of the shape can be passing them to this method.
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg", RelativeHorizontalPosition.Margin, 0,
    RelativeVerticalPosition.Margin, 0, -1, -1, WrapType.Square);

// Passing negative values as the intended dimensions will automatically define
// the shape's dimensions based on the dimensions of its image.
Assert.AreEqual(300.0d, imageShape.Width);
Assert.AreEqual(300.0d, imageShape.Height);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
```

Shows how to insert an image from the local file system into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are three ways of inserting an image from a local system filename.
// 1 -  Inline shape with a default size based on the image's original dimensions:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 -  Inline shape with custom dimensions:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 -  Floating shape with custom dimensions:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## InsertImage(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_7}

Inserts an image from a stream at the specified position and size.

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | The stream that contains the image. |
| horzPos | RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | Double | Distance in points from the origin to the left side of the image. |
| vertPos | RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | Double | Distance in points from the origin to the top side of the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | WrapType | Specifies how to wrap text around the image. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples

Shows how to insert an image from a stream into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Below are three ways of inserting an image from a stream.
    // 1 -  Inline shape with a default size based on the image's original dimensions:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 -  Inline shape with custom dimensions:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 -  Floating shape with custom dimensions:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## InsertImage(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_1}

Inserts an image from a byte array at the specified position and size.

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | Byte[] | The byte array that contains the image. |
| horzPos | RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | Double | Distance in points from the origin to the left side of the image. |
| vertPos | RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | Double | Distance in points from the origin to the top side of the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | WrapType | Specifies how to wrap text around the image. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples

Shows how to insert an image from a byte array into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // Below are three ways of inserting an image from a byte array.
    // 1 -  Inline shape with a default size based on the image's original dimensions:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 -  Inline shape with custom dimensions:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 -  Floating shape with custom dimensions:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Shows how to insert an image from a byte array into a document (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Decoding the image will convert it to the .png format.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Below are three ways of inserting an image from a byte array.
            // 1 -  Inline shape with a default size based on the image's original dimensions:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 -  Inline shape with custom dimensions:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 -  Floating shape with custom dimensions:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
