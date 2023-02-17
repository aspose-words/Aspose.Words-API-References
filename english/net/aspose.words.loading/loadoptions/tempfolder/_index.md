---
title: LoadOptions.TempFolder
second_title: Aspose.Words for .NET API Reference
description: LoadOptions property. Allows to use temporary files when reading document. By default this property is null and no temporary files are used in C#.
type: docs
weight: 150
url: /net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

Allows to use temporary files when reading document. By default this property is `null` and no temporary files are used.

```csharp
public string TempFolder { get; set; }
```

## Remarks

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when reading is complete.

## Examples

Shows how to load a document using temporary files.

```csharp
// Note that such an approach can reduce memory usage but degrades speed
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// Ensure that the directory exists and load
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

Shows how to use the hard drive instead of memory when loading a document.

```csharp
// When we load a document, various elements are temporarily stored in memory as the save operation occurs.
// We can use this option to use a temporary folder in the local file system instead,
// which will reduce our application's memory overhead.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// The specified temporary folder must exist in the local file system before the load operation.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// The folder will persist with no residual contents from the load operation.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### See Also

* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../loadoptions/)
* assembly [Aspose.Words](../../../)
