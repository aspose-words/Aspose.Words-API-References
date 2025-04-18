---
title: SaveOptions.ExportGeneratorName
linktitle: ExportGeneratorName
articleTitle: ExportGeneratorName
second_title: Aspose.Words for .NET
description: Enhance your documents with the SaveOptions ExportGeneratorName property. Embed Aspose.Words name and version for better traceability. Default, true.
type: docs
weight: 80
url: /net/aspose.words.saving/saveoptions/exportgeneratorname/
---
## SaveOptions.ExportGeneratorName property

When `true`, causes the name and version of Aspose.Words to be embedded into produced files. Default value is `true`.

```csharp
public bool ExportGeneratorName { get; set; }
```

## Examples

Shows how to disable adding name and version of Aspose.Words into produced files.

```csharp
Document doc = new Document();

// Use https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ to know how to check the result.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { ExportGeneratorName = false };

doc.Save(ArtifactsDir + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

### See Also

* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
