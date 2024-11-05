---
title: Converter.ConvertToImages
linktitle: ConvertToImages
articleTitle: ConvertToImages
second_title: Aspose.Words for .NET
description: Converter ConvertToImages method. Converts the input file pages to images in C#.
type: docs
weight: 20
url: /net/aspose.words.lowcode/converter/converttoimages/
---
## ConvertToImages(*string, string*) {#converttoimages_8}

Converts the input file pages to images.

```csharp
public static void ConvertToImages(string inputFile, string outputFile)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | String | The input file name. |
| outputFile | String | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |

## Examples

Shows how to convert document to images.

```csharp
Converter.ConvertToImages(MyDir + "Big document.docx", ArtifactsDir + "LowCode.ConvertToImages.png");

Converter.ConvertToImages(MyDir + "Big document.docx", ArtifactsDir + "LowCode.ConvertToImages.jpeg", SaveFormat.Jpeg);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
Converter.ConvertToImages(MyDir + "Big document.docx", ArtifactsDir + "LowCode.ConvertToImages.png", imageSaveOptions);
```

### See Also

* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ConvertToImages(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_9}

Converts the input file pages to images.

```csharp
public static void ConvertToImages(string inputFile, string outputFile, SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | String | The input file name. |
| outputFile | String | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |
| saveFormat | SaveFormat | Save format. Only image save formats are allowed. |

## Examples

Shows how to convert document to images.

```csharp
Converter.ConvertToImages(MyDir + "Big document.docx", ArtifactsDir + "LowCode.ConvertToImages.png");

Converter.ConvertToImages(MyDir + "Big document.docx", ArtifactsDir + "LowCode.ConvertToImages.jpeg", SaveFormat.Jpeg);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
Converter.ConvertToImages(MyDir + "Big document.docx", ArtifactsDir + "LowCode.ConvertToImages.png", imageSaveOptions);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ConvertToImages(*string, string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_10}

Converts the input file pages to images.

```csharp
public static void ConvertToImages(string inputFile, string outputFile, 
    ImageSaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | String | The input file name. |
| outputFile | String | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |
| saveOptions | ImageSaveOptions | Image save options. |

## Examples

Shows how to convert document to images.

```csharp
Converter.ConvertToImages(MyDir + "Big document.docx", ArtifactsDir + "LowCode.ConvertToImages.png");

Converter.ConvertToImages(MyDir + "Big document.docx", ArtifactsDir + "LowCode.ConvertToImages.jpeg", SaveFormat.Jpeg);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
Converter.ConvertToImages(MyDir + "Big document.docx", ArtifactsDir + "LowCode.ConvertToImages.png", imageSaveOptions);
```

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ConvertToImages(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/), string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_7}

Converts the input file pages to images.

```csharp
public static void ConvertToImages(string inputFile, LoadOptions loadOptions, string outputFile, 
    ImageSaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | String | The input file name. |
| loadOptions | LoadOptions | The input document load options. |
| outputFile | String | The output file name used to generate file name for page images using rule "outputFile_pageIndex.extension" |
| saveOptions | ImageSaveOptions | Image save options. |

### See Also

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ConvertToImages(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_5}

Converts the input file pages to images.

```csharp
public static Stream[] ConvertToImages(string inputFile, SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | String | The input file name. |
| saveFormat | SaveFormat | Save format. Only image save formats are allowed. |

### Return Value

Returns array of image streams. The streams should be disposed by the enduser.

## Examples

Shows how to convert document to images stream.

```csharp
Stream[] streams = Converter.ConvertToImages(MyDir + "Big document.docx", SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(MyDir + "Big document.docx", imageSaveOptions);

streams = Converter.ConvertToImages(new Document(MyDir + "Big document.docx"), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(MyDir + "Big document.docx"), imageSaveOptions);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ConvertToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_6}

Converts the input file pages to images.

```csharp
public static Stream[] ConvertToImages(string inputFile, ImageSaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | String | The input file name. |
| saveOptions | ImageSaveOptions | Image save options. |

### Return Value

Returns array of image streams. The streams should be disposed by the enduser.

## Examples

Shows how to convert document to images stream.

```csharp
Stream[] streams = Converter.ConvertToImages(MyDir + "Big document.docx", SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(MyDir + "Big document.docx", imageSaveOptions);

streams = Converter.ConvertToImages(new Document(MyDir + "Big document.docx"), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(MyDir + "Big document.docx"), imageSaveOptions);
```

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_3}

Converts the input stream pages to images.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| saveFormat | SaveFormat | Save format. Only image save formats are allowed. |

### Return Value

Returns array of image streams. The streams should be disposed by the enduser.

## Examples

Shows how to convert document to images from stream.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);
}
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_4}

Converts the input stream pages to images.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, ImageSaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| saveOptions | ImageSaveOptions | Image save options. |

### Return Value

Returns array of image streams. The streams should be disposed by the enduser.

## Examples

Shows how to convert document to images from stream.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);
}
```

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_2}

Converts the input stream pages to images.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, LoadOptions loadOptions, 
    ImageSaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| loadOptions | LoadOptions | The input document load options. |
| saveOptions | ImageSaveOptions | Image save options. |

### Return Value

Returns array of image streams. The streams should be disposed by the enduser.

### See Also

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages}

Converts the document pages to images.

```csharp
public static Stream[] ConvertToImages(Document doc, SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | Document | The input document. |
| saveFormat | SaveFormat | Save format. Only image save formats are allowed. |

### Return Value

Returns array of image streams. The streams should be disposed by the enduser.

## Examples

Shows how to convert document to images stream.

```csharp
Stream[] streams = Converter.ConvertToImages(MyDir + "Big document.docx", SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(MyDir + "Big document.docx", imageSaveOptions);

streams = Converter.ConvertToImages(new Document(MyDir + "Big document.docx"), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(MyDir + "Big document.docx"), imageSaveOptions);
```

### See Also

* class [Document](../../../aspose.words/document/)
* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_1}

Converts the document pages to images.

```csharp
public static Stream[] ConvertToImages(Document doc, ImageSaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | Document | The input document. |
| saveOptions | ImageSaveOptions | Image save options. |

### Return Value

Returns array of image streams. The streams should be disposed by the enduser.

## Examples

Shows how to convert document to images stream.

```csharp
Stream[] streams = Converter.ConvertToImages(MyDir + "Big document.docx", SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(MyDir + "Big document.docx", imageSaveOptions);

streams = Converter.ConvertToImages(new Document(MyDir + "Big document.docx"), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(MyDir + "Big document.docx"), imageSaveOptions);
```

### See Also

* class [Document](../../../aspose.words/document/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
