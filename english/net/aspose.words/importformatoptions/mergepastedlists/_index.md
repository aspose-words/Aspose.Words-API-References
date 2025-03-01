---
title: ImportFormatOptions.MergePastedLists
linktitle: MergePastedLists
articleTitle: MergePastedLists
second_title: Aspose.Words for .NET
description: Control list merging with the ImportFormatOptions MergePastedLists property. Easily manage pasted lists to enhance document formatting. Default, false.
type: docs
weight: 70
url: /net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

Gets or sets a boolean value that specifies whether pasted lists will be merged with surrounding lists. The default value is `false`.

```csharp
public bool MergePastedLists { get; set; }
```

## Examples

Shows how to merge lists from a documents.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### See Also

* class [ImportFormatOptions](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
