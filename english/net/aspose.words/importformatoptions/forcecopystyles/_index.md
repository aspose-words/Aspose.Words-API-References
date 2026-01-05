---
title: ImportFormatOptions.ForceCopyStyles
linktitle: ForceCopyStyles
articleTitle: ForceCopyStyles
second_title: Aspose.Words for .NET
description: Discover the ImportFormatOptions ForceCopyStyles property, control style copying in KeepSourceFormatting mode with ease. Default is false for optimal results.
type: docs
weight: 40
url: /net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

Gets or sets a boolean value indicating either to copy conflicting styles in KeepSourceFormatting mode. The default value is `false`.

```csharp
public bool ForceCopyStyles { get; set; }
```

## Remarks

By default, if a matching style already exists in a destination document, the source style formatting is expanded into direct node attributes and the style of this node is reset to a default.

When this option is set to `true`, the source style will be forcibly copied into destination document with unique name and applied to the imported node.

Note, in this case it is not guaranteed that formatting of the imported node in destination document will be preserved.

## Examples

Shows how to copy source styles with unique names forcibly.

```csharp
// Both documents contain MyStyle1 and MyStyle2, MyStyle3 exists only in a source document.
Document srcDoc = new Document(MyDir + "Styles source.docx");
Document dstDoc = new Document(MyDir + "Styles destination.docx");

ImportFormatOptions options = new ImportFormatOptions { ForceCopyStyles = true };
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

ParagraphCollection paras = dstDoc.Sections[1].Body.Paragraphs;

Assert.That("MyStyle1_0", Is.EqualTo(paras[0].ParagraphFormat.Style.Name));
Assert.That("MyStyle2_0", Is.EqualTo(paras[1].ParagraphFormat.Style.Name));
Assert.That("MyStyle3", Is.EqualTo(paras[2].ParagraphFormat.Style.Name));
```

### See Also

* class [ImportFormatOptions](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
