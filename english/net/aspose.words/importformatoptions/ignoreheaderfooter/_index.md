---
title: ImportFormatOptions.IgnoreHeaderFooter
second_title: Aspose.Words for .NET API Reference
description: ImportFormatOptions property. Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored if KeepSourceFormatting mode is used. The default value is true in C#.
type: docs
weight: 30
url: /net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored if KeepSourceFormatting mode is used. The default value is `true`.

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## Examples

Shows how to specifies ignoring or not source formatting of headers/footers content.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### See Also

* class [ImportFormatOptions](../)
* namespace [Aspose.Words](../../importformatoptions/)
* assembly [Aspose.Words](../../../)
