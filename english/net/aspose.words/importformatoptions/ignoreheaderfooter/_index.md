---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: Aspose.Words for .NET
description: ImportFormatOptions IgnoreHeaderFooter property. Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored if KeepSourceFormatting mode is used. The default value is true in C#.
type: docs
weight: 40
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

// If 'IgnoreHeaderFooter' is false then the original formatting for header/footer content
// from "Header and footer types.docx" will be used.
// If 'IgnoreHeaderFooter' is true then the formatting for header/footer content
// from "Document.docx" will be used.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### See Also

* class [ImportFormatOptions](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
