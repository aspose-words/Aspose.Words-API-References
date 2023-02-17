---
title: RtfSaveOptions.ExportCompactSize
second_title: Aspose.Words for .NET API Reference
description: RtfSaveOptions property. Allows to make output RTF documents smaller in size but if they contain RTL righttoleft text it will not be displayed correctly. Default value is false in C#.
type: docs
weight: 20
url: /net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Allows to make output RTF documents smaller in size, but if they contain RTL (right-to-left) text, it will not be displayed correctly. Default value is `false`.

```csharp
public bool ExportCompactSize { get; set; }
```

## Remarks

If the document that you want to convert to RTF using Aspose.Words does not contain right-to-left text in languages like Arabic, then you can set this option to `true` to reduce the size of the resulting RTF.

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

* class [RtfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../rtfsaveoptions/)
* assembly [Aspose.Words](../../../)
