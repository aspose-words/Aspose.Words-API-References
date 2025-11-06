---
title: MergeFormatMode Enum
linktitle: MergeFormatMode
articleTitle: MergeFormatMode
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.LowCode.MergeFormatMode enum to optimize document merging. Enhance formatting control when combining multiple files effortlessly.
type: docs
weight: 4320
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
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### See Also

* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
