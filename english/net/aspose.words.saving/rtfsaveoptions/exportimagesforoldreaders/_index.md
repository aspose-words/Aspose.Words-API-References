---
title: RtfSaveOptions.ExportImagesForOldReaders
linktitle: ExportImagesForOldReaders
articleTitle: ExportImagesForOldReaders
second_title: Aspose.Words for .NET
description: Optimize your RTF documents with the ExportImagesForOldReaders property. Control keyword inclusion for legacy readers, impacting file size and performance.
type: docs
weight: 30
url: /net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

Specifies whether the keywords for "old readers" are written to RTF or not. This can significantly affect the size of the RTF document. Default value is `true`.

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

## Remarks

"Old readers" are pre-Microsoft Word 97 applications and also WordPad. When this option is `true` Aspose.Words writes additional RTF keywords. These keywords allow the document to be displayed correctly when opened in an "old reader" application, but can significantly increase the size of the document.

If you set this option to `false`, then only images in WMF, EMF and BMP formats will be displayed in "old readers".

## Examples

Shows how to save a document to .rtf with custom options.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Create an "RtfSaveOptions" object to pass to the document's "Save" method to modify how we save it to an RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.That(options.SaveFormat, Is.EqualTo(SaveFormat.Rtf));

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
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
