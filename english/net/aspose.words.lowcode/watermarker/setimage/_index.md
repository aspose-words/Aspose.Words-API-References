---
title: Watermarker.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words for .NET
description: Enhance your documents with the Watermarker SetImage method. Effortlessly add custom image watermarks for a professional touch.
type: docs
weight: 20
url: /net/aspose.words.lowcode/watermarker/setimage/
---
## SetImage(*string, string, string*) {#setimage_6}

Adds an image watermark into the document.

```csharp
public static void SetImage(string inputFileName, string outputFileName, 
    string watermarkImageFileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| watermarkImageFileName | String | Image that is displayed as a watermark. |

## Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## Examples

Shows how to insert watermark image to the document.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### See Also

* class [Watermarker](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## SetImage(*string, string, string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_7}

Adds an image watermark into the document with options.

```csharp
public static void SetImage(string inputFileName, string outputFileName, 
    string watermarkImageFileName, ImageWatermarkOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| watermarkImageFileName | String | Image that is displayed as a watermark. |
| options | ImageWatermarkOptions | Defines additional options for the image watermark. |

## Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## Examples

Shows how to insert watermark image to the document.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### See Also

* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## SetImage(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_4}

Adds an image watermark into the document with options and specified save format.

```csharp
public static void SetImage(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string watermarkImageFileName, ImageWatermarkOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| saveFormat | SaveFormat | The save format. |
| watermarkImageFileName | String | Image that is displayed as a watermark. |
| options | ImageWatermarkOptions | Defines additional options for the image watermark. |

## Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

## Examples

Shows how to insert watermark image to the document.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.2.docx", SaveFormat.Docx, watermarkImage);

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
Watermarker.SetImage(doc, ArtifactsDir + "LowCode.SetWatermarkText.4.docx", SaveFormat.Docx, watermarkImage, options);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## SetImage(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_5}

Adds an image watermark into the document with options and specified save format.

```csharp
public static void SetImage(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string watermarkImageFileName, ImageWatermarkOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| saveOptions | SaveOptions | The save options. |
| watermarkImageFileName | String | Image that is displayed as a watermark. |
| options | ImageWatermarkOptions | Defines additional options for the image watermark. |

## Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Image, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage}

Adds an image watermark into the document from streams with options.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Image watermarkImage, ImageWatermarkOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| outputStream | Stream | The output stream. |
| saveFormat | SaveFormat | The save format. |
| watermarkImage | Image | Image that is displayed as a watermark. |
| options | ImageWatermarkOptions | Defines additional options for the image watermark. |

## Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

## Examples

Shows how to insert watermark image to the document from a stream.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.SetWatermarkText.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetImage(streamIn, streamOut, SaveFormat.Docx, System.Drawing.Image.FromFile(ImageDir + "Logo.jpg"));
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.SetWatermarkText.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetImage(streamIn, streamOut, SaveFormat.Docx, System.Drawing.Image.FromFile(ImageDir + "Logo.jpg"), new ImageWatermarkOptions() { Scale = 50 });
}
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Image, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_2}

Adds an image watermark into the document from streams with options.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Image watermarkImage, ImageWatermarkOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| outputStream | Stream | The output stream. |
| saveOptions | SaveOptions | The save options. |
| watermarkImage | Image | Image that is displayed as a watermark. |
| options | ImageWatermarkOptions | Defines additional options for the image watermark. |

## Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_1}

Adds an image watermark into the document from streams with options.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| outputStream | Stream | The output stream. |
| saveFormat | SaveFormat | The save format. |
| watermarkImageStream | Stream | Image stream that is displayed as a watermark. |
| options | ImageWatermarkOptions | Defines additional options for the image watermark. |

## Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## SetImage(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setimage_3}

Adds an image watermark into the document from streams with options.

```csharp
public static void SetImage(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| outputStream | Stream | The output stream. |
| saveOptions | SaveOptions | The save options. |
| watermarkImageStream | Stream | Image stream that is displayed as a watermark. |
| options | ImageWatermarkOptions | Defines additional options for the image watermark. |

## Remarks

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), only the first page of the output will be saved to the specified stream.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF to the specified stream.

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
