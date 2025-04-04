---
title: Watermarker.SetWatermarkToImages
linktitle: SetWatermarkToImages
articleTitle: SetWatermarkToImages
second_title: Aspose.Words for .NET
description: Enhance your images with our Watermarker Set method, adding customizable text watermarks for a professional touch and seamless output.
type: docs
weight: 40
url: /net/aspose.words.lowcode/watermarker/setwatermarktoimages/
---
## SetWatermarkToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#setwatermarktoimages_3}

Adds a text watermark into the document with options. Renders the output to images.

```csharp
public static Stream[] SetWatermarkToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| saveOptions | ImageSaveOptions | The save options. |
| watermarkText | String | Text that is displayed as a watermark. |
| options | TextWatermarkOptions | Defines additional options for the text watermark. |

## Examples

Shows how to insert watermark text to the document and save result to images.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Stream[] images = Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), watermarkText);

TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
images = Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), watermarkText, watermarkOptions);
```

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## SetWatermarkToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#setwatermarktoimages_1}

Adds a text watermark into the document with options. Renders the output to images.

```csharp
public static Stream[] SetWatermarkToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input file stream. |
| saveOptions | ImageSaveOptions | The save options. |
| watermarkText | String | Text that is displayed as a watermark. |
| options | TextWatermarkOptions | Defines additional options for the text watermark. |

## Examples

Shows how to insert watermark text to the document from the stream and save result to images.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), watermarkText);

    TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
    watermarkOptions.Color = Color.Red;
    images = Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), watermarkText, watermarkOptions);
}
```

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## SetWatermarkToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), byte[], [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setwatermarktoimages_2}

Adds an image watermark into the document with options. Renders the output to images.

```csharp
public static Stream[] SetWatermarkToImages(string inputFileName, ImageSaveOptions saveOptions, 
    byte[] watermarkImageBytes, ImageWatermarkOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| saveOptions | ImageSaveOptions | The save options. |
| watermarkImageBytes | Byte[] | Image bytes that is displayed as a watermark. |
| options | ImageWatermarkOptions | Defines additional options for the image watermark. |

## Examples

Shows how to insert watermark image to the document and save result to images.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), File.ReadAllBytes(watermarkImage));

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), File.ReadAllBytes(watermarkImage), options);
```

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## SetWatermarkToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setwatermarktoimages}

Adds an image watermark into the document with options. Renders the output to images.

```csharp
public static Stream[] SetWatermarkToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| saveOptions | ImageSaveOptions | The save options. |
| watermarkImageStream | Stream | Image stream that is displayed as a watermark. |
| options | ImageWatermarkOptions | Defines additional options for the image watermark. |

## Examples

Shows how to insert watermark image to the document from a stream and save result to images.

```csharp
string watermarkImage = ImageDir + "Logo.jpg";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream imageStream = new FileStream(watermarkImage, FileMode.Open, FileAccess.Read))
    {
        Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), imageStream);
        Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), imageStream, new ImageWatermarkOptions() { Scale = 50 });
    }
}
```

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
