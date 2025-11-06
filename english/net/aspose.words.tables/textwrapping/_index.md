---
title: TextWrapping Enum
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Tables.TextWrapping enum for efficient text wrapping around tables. Enhance your document formatting with ease!
type: docs
weight: 7300
url: /net/aspose.words.tables/textwrapping/
---
## TextWrapping enumeration

Specifies how text is wrapped around the table.

```csharp
public enum TextWrapping
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | Text and table is displayed in the order of their appearance in the document. |
| Around | `1` | Text is wrapped around the table occupying available side space. |
| Default | `0` | Default value. |

## Examples

Shows how to work with table text wrapping.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

builder.Font.Size = 16;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Set the "TextWrapping" property to "TextWrapping.Around" to get the table to wrap text around it,
// and push it down into the paragraph below by setting the position.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### See Also

* namespace [Aspose.Words.Tables](../../aspose.words.tables/)
* assembly [Aspose.Words](../../)
