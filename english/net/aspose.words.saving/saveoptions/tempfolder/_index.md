---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words for .NET
description: Optimize your document saving with the SaveOptions TempFolder property, which designates a folder for temporary DOC and DOCX files, enhancing efficiency.
type: docs
weight: 140
url: /net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is `null` and no temporary files are used.

```csharp
public string TempFolder { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| OutOfMemoryException | Throw if you are saving a very large document (thousands of pages) and/or processing many documents at the same time. The memory spike during saving can be significant enough to cause the exception. |

## Remarks

When Aspose.Words saves a document, it needs to create temporary internal structures. By default, these internal structures are created in memory and the memory usage spikes for a short period while the document is being saved. When saving is complete, the memory is freed and reclaimed by the garbage collector.

Specifying a temporary folder using `TempFolder` will cause Aspose.Words to keep the internal structures in temporary files instead of memory. It reduces the memory usage during saving, but will decrease the save performance.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when saving is complete.

## Examples

Shows how to use the hard drive instead of memory when saving a document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// When we save a document, various elements are temporarily stored in memory as the save operation is taking place.
// We can use this option to use a temporary folder in the local file system instead,
// which will reduce our application's memory overhead.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// The specified temporary folder must exist in the local file system before the save operation.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// The folder will persist with no residual contents from the load operation.
Assert.That(Directory.GetFiles(options.TempFolder).Length, Is.EqualTo(0));
```

### See Also

* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
