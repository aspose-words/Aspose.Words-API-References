---
title: FileFormatUtil Class
linktitle: FileFormatUtil
articleTitle: FileFormatUtil
second_title: Aspose.Words for .NET
description: Effortlessly manage file formats with Aspose.Words.FileFormatUtil. Detect formats and convert extensions seamlessly for enhanced productivity.
type: docs
weight: 3220
url: /net/aspose.words/fileformatutil/
---
## FileFormatUtil class

Provides utility methods for working with file formats, such as detecting file format or converting file extensions to/from file format enums.

To learn more, visit the [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) documentation article.

```csharp
public static class FileFormatUtil
```

## Methods

| Name | Description |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(*string*) | Converts IANA content type into a load format enumerated value. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(*string*) | Converts IANA content type into a save format enumerated value. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(*Stream*) | Detects and returns the information about a format of a document stored in a stream. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(*string*) | Detects and returns the information about a format of a document stored in a disk file. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(*string*) | Converts a file name extension into a [`SaveFormat`](../saveformat/) value. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(*[ImageType](../../aspose.words.drawing/imagetype/)*) | Converts an Aspose.Words image type enumerated value into a file extension. The returned extension is a lower-case string with a leading dot. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(*[LoadFormat](../loadformat/)*) | Converts a load format enumerated value into a file extension. The returned extension is a lower-case string with a leading dot. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(*[LoadFormat](../loadformat/)*) | Converts a [`LoadFormat`](../loadformat/) value to a [`SaveFormat`](../saveformat/) value if possible. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(*[SaveFormat](../saveformat/)*) | Converts a save format enumerated value into a file extension. The returned extension is a lower-case string with a leading dot. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(*[SaveFormat](../saveformat/)*) | Converts a [`SaveFormat`](../saveformat/) value to a [`LoadFormat`](../loadformat/) value if possible. |

## Examples

Shows how to detect encoding in an html file.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.That(info.LoadFormat, Is.EqualTo(LoadFormat.Html));

// The Encoding property is used only when we create a FileFormatInfo object for an html document.
Assert.That(info.Encoding.EncodingName, Is.EqualTo("Western European (Windows)"));
Assert.That(info.Encoding.CodePage, Is.EqualTo(1252));
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
