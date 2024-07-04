---
title: TextColumnCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: TextColumnCollection Count property. Gets the number of columns in the section of a document in C#.
type: docs
weight: 10
url: /net/aspose.words/textcolumncollection/count/
---
## TextColumnCollection.Count property

Gets the number of columns in the section of a document.

```csharp
public int Count { get; }
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

* class [TextColumnCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
