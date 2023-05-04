---
title: PageSetup.TextColumns
linktitle: TextColumns
articleTitle: TextColumns
second_title: Aspose.Words for .NET
description: PageSetup TextColumns property. Returns a collection that represents the set of text columns in C#.
type: docs
weight: 420
url: /net/aspose.words/pagesetup/textcolumns/
---
## PageSetup.TextColumns property

Returns a collection that represents the set of text columns.

```csharp
public TextColumnCollection TextColumns { get; }
```

## Examples

Shows how to create multiple evenly spaced columns in a section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### See Also

* class [TextColumnCollection](../../textcolumncollection/)
* class [PageSetup](../)
* namespace [Aspose.Words](../../pagesetup/)
* assembly [Aspose.Words](../../../)
