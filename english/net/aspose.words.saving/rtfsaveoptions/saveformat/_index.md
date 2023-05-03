---
title: RtfSaveOptions.SaveFormat
linktitle: SaveFormat
second_title: Aspose.Words for .NET API Reference
description: RtfSaveOptions SaveFormat property. Specifies the format in which the document will be saved if this save options object is used. Can only be Rtf in C#.
type: docs
weight: 40
url: /net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## SaveFormat property

Specifies the format in which the document will be saved if this save options object is used. Can only be Rtf.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Examples

Shows how to save a document to .rtf with custom options.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Create an "RtfSaveOptions" object to pass to the document's "Save" method to modify how we save it to an RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Set the "ExportCompactSize" property to "true" to
// reduce the saved document's size at the cost of right-to-left text compatibility.
options.ExportCompactSize = true;

// Set the "ExportImagesFotOldReaders" property to "true" to use extra keywords to ensure that our document is
// compatible with pre-Microsoft Word 97 readers and WordPad.
// Set the "ExportImagesFotOldReaders" property to "false" to reduce the size of the document,
// but prevent old readers from being able to read any non-metafile or BMP images that the document may contain.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../rtfsaveoptions/)
* assembly [Aspose.Words](../../../)
