---
title: Converter.Convert
linktitle: Convert
articleTitle: Convert
second_title: Aspose.Words for .NET
description: Converter Convert method. Converts the given input document into the output document using specified input output file names and its extensions in C#.
type: docs
weight: 10
url: /net/aspose.words.lowcode/converter/convert/
---
## Convert(*string, string*) {#convert_4}

Converts the given input document into the output document using specified input output file names and its extensions.

```csharp
public static void Convert(string inputFile, string outputFile)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | String | The input file name. |
| outputFile | String | The output file name. |

## Examples

Shows how to convert documents with a single line of code.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### See Also

* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Convert(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#convert_5}

Converts the given input document into the output document using specified input output file names and the final document format.

```csharp
public static void Convert(string inputFile, string outputFile, SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | String | The input file name. |
| outputFile | String | The output file name. |
| saveFormat | SaveFormat | The save format. |

## Examples

Shows how to convert documents with a single line of code.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Convert(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_6}

Converts the given input document into the output document using specified input output file names and save options.

```csharp
public static void Convert(string inputFile, string outputFile, SaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | String | The input file name. |
| outputFile | String | The output file name. |
| saveOptions | SaveOptions | The save options. |

## Examples

Shows how to convert documents with a single line of code.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Convert(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_3}

Converts the given input document into the output document using specified input output file names its load/save options.

```csharp
public static void Convert(string inputFile, LoadOptions loadOptions, string outputFile, 
    SaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | String | The input file name. |
| loadOptions | LoadOptions | The input document load options. |
| outputFile | String | The output file name. |
| saveOptions | SaveOptions | The save options. |

## Examples

Shows how to convert documents with a single line of code.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### See Also

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Convert(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#convert_1}

Converts the given input document into a single output document using specified input and output streams.

```csharp
public static void Convert(Stream inputStream, Stream outputStream, SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input stream. |
| outputStream | Stream | The output stream. |
| saveFormat | SaveFormat | The save format. |

## Examples

Shows how to convert documents with a single line of code (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Convert(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_2}

Converts the given input document into a single output document using specified input and output streams.

```csharp
public static void Convert(Stream inputStream, Stream outputStream, SaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input streams. |
| outputStream | Stream | The output stream. |
| saveOptions | SaveOptions | The save options. |

## Examples

Shows how to convert documents with a single line of code (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Convert(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert}

Converts the given input document into a single output document using specified input and output streams.

```csharp
public static void Convert(Stream inputStream, LoadOptions loadOptions, Stream outputStream, 
    SaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input streams. |
| loadOptions | LoadOptions | The input document load options. |
| outputStream | Stream | The output stream. |
| saveOptions | SaveOptions | The save options. |

## Examples

Shows how to convert documents with a single line of code (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### See Also

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
