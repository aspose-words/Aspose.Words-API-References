---
title: FileFormatUtil.ContentTypeToSaveFormat
linktitle: ContentTypeToSaveFormat
articleTitle: ContentTypeToSaveFormat
second_title: Aspose.Words for .NET
description: Convert IANA content types to save format values effortlessly with the FileFormatUtil ContentTypeToSaveFormat method. Streamline your file handling today!
type: docs
weight: 20
url: /net/aspose.words/fileformatutil/contenttypetosaveformat/
---
## FileFormatUtil.ContentTypeToSaveFormat method

Converts IANA content type into a save format enumerated value.

```csharp
public static SaveFormat ContentTypeToSaveFormat(string contentType)
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentException | Throws when cannot convert. |

## Examples

Shows how to find the corresponding Aspose load/save format from each media type string.

```csharp
// The ContentTypeToSaveFormat/ContentTypeToLoadFormat methods only accept official IANA media type names, also known as MIME types. 
// All valid media types are listed here: https://www.iana.org/assignments/media-types/media-types.xhtml.

// Trying to associate a SaveFormat with a partial media type string will not work.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("jpeg"));

// If Aspose.Words does not have a corresponding save/load format for a content type, an exception will also be thrown.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("application/zip"));

// Files of the types listed below can be saved, but not loaded using Aspose.Words.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToLoadFormat("image/jpeg"));

Assert.That(FileFormatUtil.ContentTypeToSaveFormat("image/jpeg"), Is.EqualTo(SaveFormat.Jpeg));
Assert.That(FileFormatUtil.ContentTypeToSaveFormat("image/png"), Is.EqualTo(SaveFormat.Png));
Assert.That(FileFormatUtil.ContentTypeToSaveFormat("image/tiff"), Is.EqualTo(SaveFormat.Tiff));
Assert.That(FileFormatUtil.ContentTypeToSaveFormat("image/gif"), Is.EqualTo(SaveFormat.Gif));
Assert.That(FileFormatUtil.ContentTypeToSaveFormat("image/x-emf"), Is.EqualTo(SaveFormat.Emf));
Assert.That(FileFormatUtil.ContentTypeToSaveFormat("application/vnd.ms-xpsdocument"), Is.EqualTo(SaveFormat.Xps));
Assert.That(FileFormatUtil.ContentTypeToSaveFormat("application/pdf"), Is.EqualTo(SaveFormat.Pdf));
Assert.That(FileFormatUtil.ContentTypeToSaveFormat("image/svg+xml"), Is.EqualTo(SaveFormat.Svg));
Assert.That(FileFormatUtil.ContentTypeToSaveFormat("application/epub+zip"), Is.EqualTo(SaveFormat.Epub));

// For file types that can be saved and loaded, we can match a media type to both a load format and a save format.
Assert.That(FileFormatUtil.ContentTypeToLoadFormat("application/msword"), Is.EqualTo(LoadFormat.Doc));
Assert.That(FileFormatUtil.ContentTypeToSaveFormat("application/msword"), Is.EqualTo(SaveFormat.Doc));

Assert.That(FileFormatUtil.ContentTypeToLoadFormat(
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document"), Is.EqualTo(LoadFormat.Docx));
Assert.That(FileFormatUtil.ContentTypeToSaveFormat(
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document"), Is.EqualTo(SaveFormat.Docx));

Assert.That(FileFormatUtil.ContentTypeToLoadFormat("text/plain"), Is.EqualTo(LoadFormat.Text));
Assert.That(FileFormatUtil.ContentTypeToSaveFormat("text/plain"), Is.EqualTo(SaveFormat.Text));

Assert.That(FileFormatUtil.ContentTypeToLoadFormat("application/rtf"), Is.EqualTo(LoadFormat.Rtf));
Assert.That(FileFormatUtil.ContentTypeToSaveFormat("application/rtf"), Is.EqualTo(SaveFormat.Rtf));

Assert.That(FileFormatUtil.ContentTypeToLoadFormat("text/html"), Is.EqualTo(LoadFormat.Html));
Assert.That(FileFormatUtil.ContentTypeToSaveFormat("text/html"), Is.EqualTo(SaveFormat.Html));

Assert.That(FileFormatUtil.ContentTypeToLoadFormat("multipart/related"), Is.EqualTo(LoadFormat.Mhtml));
Assert.That(FileFormatUtil.ContentTypeToSaveFormat("multipart/related"), Is.EqualTo(SaveFormat.Mhtml));
```

### See Also

* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
