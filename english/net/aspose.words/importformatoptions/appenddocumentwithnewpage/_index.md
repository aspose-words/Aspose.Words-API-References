---
title: ImportFormatOptions.AppendDocumentWithNewPage
linktitle: AppendDocumentWithNewPage
articleTitle: AppendDocumentWithNewPage
second_title: Aspose.Words for .NET
description: Control document merging by forcing imported sections to start on a new page when appending documents in Aspose.Words.
type: docs
weight: 30
url: /net/aspose.words/importformatoptions/appenddocumentwithnewpage/
---
## ImportFormatOptions.AppendDocumentWithNewPage property

Gets or sets a boolean value indicating whether to change a first imported section type to the NewPage forcibly when call [`AppendDocument`](../../document/appenddocument/).

The default value is `true`.

```csharp
public bool AppendDocumentWithNewPage { get; set; }
```

## Remarks

Please note that this option is only relevant for the [`AppendDocument`](../../document/appenddocument/) method and has no effect on other import-related methods.

## Examples

Shows how to preserve original section type.

```csharp
Document dstDoc = new Document();
Document srcDoc = new Document();

srcDoc.FirstSection.PageSetup.SectionStart = SectionStart.Continuous;

ImportFormatOptions options = new ImportFormatOptions { AppendDocumentWithNewPage = false };
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

Assert.That(dstDoc.Sections[1].PageSetup.SectionStart, Is.EqualTo(SectionStart.Continuous));
```

### See Also

* class [ImportFormatOptions](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
