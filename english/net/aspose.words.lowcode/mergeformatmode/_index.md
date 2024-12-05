---
title: MergeFormatMode Enum
linktitle: MergeFormatMode
articleTitle: MergeFormatMode
second_title: Aspose.Words for .NET
description: Aspose.Words.LowCode.MergeFormatMode enum. Specifies how formatting is merged when combining multiple documents in C#.
type: docs
weight: 4210
url: /net/aspose.words.lowcode/mergeformatmode/
---
## MergeFormatMode enumeration

Specifies how formatting is merged when combining multiple documents.

```csharp
public enum MergeFormatMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| MergeFormatting | `0` | Combine the formatting of the merged documents. |
| KeepSourceFormatting | `1` | Means that the source document will retain its original formatting, such as font styles, sizes, colors, indents, and any other formatting elements applied to its content. |
| KeepSourceLayout | `2` | Preserve the layout of the original documents in the final document. |

## Examples

Shows how to merge documents into a single output document.

```csharp
//There is a several ways to merge documents:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### See Also

* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
