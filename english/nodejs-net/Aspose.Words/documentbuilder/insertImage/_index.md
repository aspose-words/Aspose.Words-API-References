---
title: DocumentBuilder.insertImage method
linktitle: insertImage method
articleTitle: insertImage method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder.insertImage method"
type: docs
weight: 400
url: /nodejs-net/Aspose.Words/documentbuilder/insertImage/
---

## insertImage(image) {#jsimage}

```js
insertImage(image: Aspose.Words.JSImage)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | [JSImage](../../jsimage/) |  |

## insertImage(image, width, height) {#jsimage_number_number}

```js
insertImage(image: Aspose.Words.JSImagewidth: numberheight: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | [JSImage](../../jsimage/) |  |
| width | number |  |
| height | number |  |

## insertImage(image, horzPos, left, vertPos, top, width, height, wrapType) {#jsimage_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype}

```js
insertImage(image: Aspose.Words.JSImagehorzPos: Aspose.Words.Drawing.RelativeHorizontalPositionleft: numbervertPos: Aspose.Words.Drawing.RelativeVerticalPositiontop: numberwidth: numberheight: numberwrapType: Aspose.Words.Drawing.WrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | [JSImage](../../jsimage/) |  |
| horzPos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) |  |
| left | number |  |
| vertPos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) |  |
| top | number |  |
| width | number |  |
| height | number |  |
| wrapType | [WrapType](../../../aspose.words.drawing/wraptype/) |  |

## insertImage(fileName) {#string}

Inserts an image from a file or URL into the document. The image is inserted inline and at 100% scale.


```js
insertImage(fileName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | The file with the image. Can be any valid local or remote URI. |

### Remarks

This overload will automatically download the image before inserting into the document
if you specify a remote URI.

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insertImage(stream) {#buffer}

Inserts an image from a stream into the document. The image is inserted inline and at 100% scale.


```js
insertImage(stream: Buffer)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | The stream that contains the image. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insertImage(imageBytes) {#number[]}

Inserts an image from a byte array into the document. The image is inserted inline and at 100% scale.


```js
insertImage(imageBytes: number[])
```

| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | number[] | The byte array that contains the image. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insertImage(fileName, width, height) {#string_number_number}

Inserts an inline image from a file or URL into the document and scales it to the specified size.


```js
insertImage(fileName: stringwidth: numberheight: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | The file that contains the image. |
| width | number | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | number | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insertImage(stream, width, height) {#buffer_number_number}

Inserts an inline image from a stream into the document and scales it to the specified size.


```js
insertImage(stream: Bufferwidth: numberheight: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | The stream that contains the image. |
| width | number | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | number | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insertImage(imageBytes, width, height) {#number[]_number_number}

Inserts an inline image from a byte array into the document and scales it to the specified size.


```js
insertImage(imageBytes: number[]width: numberheight: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | number[] | The byte array that contains the image. |
| width | number | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | number | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insertImage(fileName, horzPos, left, vertPos, top, width, height, wrapType) {#string_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype}

Inserts an image from a file or URL at the specified position and size.


```js
insertImage(fileName: stringhorzPos: Aspose.Words.Drawing.RelativeHorizontalPositionleft: numbervertPos: Aspose.Words.Drawing.RelativeVerticalPositiontop: numberwidth: numberheight: numberwrapType: Aspose.Words.Drawing.WrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | The file that contains the image. |
| horzPos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) | Specifies where the distance to the image is measured from. |
| left | number | Distance in points from the origin to the left side of the image. |
| vertPos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) | Specifies where the distance to the image measured from. |
| top | number | Distance in points from the origin to the top side of the image. |
| width | number | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | number | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | [WrapType](../../../aspose.words.drawing/wraptype/) | Specifies how to wrap text around the image. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insertImage(stream, horzPos, left, vertPos, top, width, height, wrapType) {#buffer_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype}

Inserts an image from a stream at the specified position and size.


```js
insertImage(stream: BufferhorzPos: Aspose.Words.Drawing.RelativeHorizontalPositionleft: numbervertPos: Aspose.Words.Drawing.RelativeVerticalPositiontop: numberwidth: numberheight: numberwrapType: Aspose.Words.Drawing.WrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | The stream that contains the image. |
| horzPos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) | Specifies where the distance to the image is measured from. |
| left | number | Distance in points from the origin to the left side of the image. |
| vertPos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) | Specifies where the distance to the image measured from. |
| top | number | Distance in points from the origin to the top side of the image. |
| width | number | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | number | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | [WrapType](../../../aspose.words.drawing/wraptype/) | Specifies how to wrap text around the image. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insertImage(imageBytes, horzPos, left, vertPos, top, width, height, wrapType) {#number[]_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype}

Inserts an image from a byte array at the specified position and size.


```js
insertImage(imageBytes: number[]horzPos: Aspose.Words.Drawing.RelativeHorizontalPositionleft: numbervertPos: Aspose.Words.Drawing.RelativeVerticalPositiontop: numberwidth: numberheight: numberwrapType: Aspose.Words.Drawing.WrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | number[] | The byte array that contains the image. |
| horzPos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) | Specifies where the distance to the image is measured from. |
| left | number | Distance in points from the origin to the left side of the image. |
| vertPos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) | Specifies where the distance to the image measured from. |
| top | number | Distance in points from the origin to the top side of the image. |
| width | number | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | number | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | [WrapType](../../../aspose.words.drawing/wraptype/) | Specifies how to wrap text around the image. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../aspose.words.drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## Examples

Shows how to insert an image from the local file system into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Below are three ways of inserting an image from a local system filename.
// 1 -  Inline shape with a default size based on the image's original dimensions:
builder.insertImage(base.imageDir + "Logo.jpg");

builder.insertBreak(aw.BreakType.PageBreak);

// 2 -  Inline shape with custom dimensions:
builder.insertImage(base.imageDir + "Transparent background logo.png", aw.ConvertUtil.pixelToPoint(250), aw.ConvertUtil.pixelToPoint(144));

builder.insertBreak(aw.BreakType.PageBreak);

// 3 -  Floating shape with custom dimensions:
builder.insertImage(base.imageDir + "Windows MetaFile.wmf", aw.Drawing.RelativeHorizontalPosition.Margin, 100,  aw.Drawing.RelativeVerticalPosition.Margin, 100, 200, 100, aw.Drawing.WrapType.Square);

doc.save(base.artifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

Shows how to determine which image will be inserted.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.insertImage(base.imageDir + "Scalable Vector Graphics.svg");

// Aspose.words insert SVG image to the document as PNG with svgBlip extension
// that contains the original vector SVG image representation.
doc.save(base.artifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.words insert SVG image to the document as PNG, just like Microsoft Word does for old format.
doc.save(base.artifactsDir + "DocumentBuilderImages.InsertSvgImage.svg.doc");

doc.compatibilityOptions.optimizeFor(aw.Settings.MsWordVersion.Word2003);

// Aspose.words insert SVG image to the document as EMF metafile to keep the image in vector representation.
doc.save(base.artifactsDir + "DocumentBuilderImages.InsertSvgImage.emf.docx");
```

Shows how to insert gif image to the document.

```js
let builder = new aw.DocumentBuilder();

// We can insert gif image using path or bytes array.
// It works only if DocumentBuilder optimized to Word version 2010 or higher.
// Note, that access to the image bytes causes conversion Gif to Png.
let gifImage = builder.insertImage(base.imageDir + "Graphics Interchange Format.gif");

gifImage = builder.insertImage(fs.readFileSync(base.imageDir + "Graphics Interchange Format.gif"));

builder.document.save(base.artifactsDir + "InsertGif.docx");
```

Shows how to insert a shape with an image into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Below are two locations where the document builder's "InsertShape" method
// can source the image that the shape will display.
// 1 -  Pass a local file system filename of an image file:
builder.write("Image from local file: ");
builder.insertImage(base.imageDir + "Logo.jpg");
builder.writeln();

// 2 -  Pass a URL which points to an image.
builder.write("Image from a URL: ");
builder.insertImage(base.imageUrl.toString());
builder.writeln();

doc.save(base.artifactsDir + "Image.FromUrl.docx");
```

Shows how to insert a floating image to the center of a page.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
let shape = builder.insertImage(base.imageDir + "Logo.jpg");
shape.wrapType = aw.Drawing.WrapType.None;
shape.behindText = true;
shape.relativeHorizontalPosition = aw.Drawing.RelativeHorizontalPosition.Page;
shape.relativeVerticalPosition = aw.Drawing.RelativeVerticalPosition.Page;
shape.horizontalAlignment = aw.Drawing.HorizontalAlignment.Center;
shape.verticalAlignment = aw.Drawing.VerticalAlignment.Center;

doc.save(base.artifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Shows how to insert WebP image.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.insertImage(base.imageDir + "WebP image.webp");

doc.save(base.artifactsDir + "Image.InsertWebpImage.docx");
```

Shows how to insert an image from a stream into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let stream = fs.readFileSync(base.imageDir + "Logo.jpg");
// Below are three ways of inserting an image from a stream.
// 1 -  Inline shape with a default size based on the image's original dimensions:
builder.insertImage(stream);

builder.insertBreak(aw.BreakType.PageBreak);

// 2 -  Inline shape with custom dimensions:
builder.insertImage(stream, aw.ConvertUtil.pixelToPoint(250), aw.ConvertUtil.pixelToPoint(144));

builder.insertBreak(aw.BreakType.PageBreak);

// 3 -  Floating shape with custom dimensions:
builder.insertImage(stream, aw.Drawing.RelativeHorizontalPosition.Margin, 100, aw.Drawing.RelativeVerticalPosition.Margin, 100, 200, 100, aw.Drawing.WrapType.Square);

doc.save(base.artifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

Shows how to insert a shape with an image from a stream into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let stream = fs.createReadStream(base.imageDir + "Logo.jpg")
builder.write("Image from stream: ");
builder.insertImage(stream);

doc.save(base.artifactsDir + "Image.FromStream.docx");
```

Shows how to insert an image.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// There are two ways of using a document builder to source an image and then insert it as a floating shape.
// 1 -  From a file in the local file system:
builder.insertImage(base.imageDir + "Transparent background logo.png", aw.Drawing.RelativeHorizontalPosition.Margin, 100,
  aw.Drawing.RelativeVerticalPosition.Margin, 0, 200, 200, aw.Drawing.WrapType.Square);

// 2 -  From a URL:
builder.insertImage(base.imageUrl.toString(), aw.Drawing.RelativeHorizontalPosition.Margin, 100,
  aw.Drawing.RelativeVerticalPosition.Margin, 250, 200, 200, aw.Drawing.WrapType.Square);

doc.save(base.artifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

Shows how to insert an image from the local file system into a document while preserving its dimensions.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// The InsertImage method creates a floating shape with the passed image in its image data.
// We can specify the dimensions of the shape can be passing them to this method.
let imageShape = builder.insertImage(base.imageDir + "Logo.jpg", aw.Drawing.RelativeHorizontalPosition.Margin, 0,
  aw.Drawing.RelativeVerticalPosition.Margin, 0, -1, -1, aw.Drawing.WrapType.Square);

// Passing negative values as the intended dimensions will automatically define
// the shape's dimensions based on the dimensions of its image.
expect(imageShape.width).toEqual(300.0);
expect(imageShape.height).toEqual(300.0);

doc.save(base.artifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

