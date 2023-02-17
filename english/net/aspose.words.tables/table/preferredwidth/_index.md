---
title: Table.PreferredWidth
second_title: Aspose.Words for .NET API Reference
description: Table property. Gets or sets the table preferred width in C#.
type: docs
weight: 220
url: /net/aspose.words.tables/table/preferredwidth/
---
## Table.PreferredWidth property

Gets or sets the table preferred width.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## Remarks

The default value is [`Auto`](../../preferredwidth/auto/).

## Examples

Shows how to set a table to auto fit to 50% of the width of the page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

### See Also

* class [PreferredWidth](../../preferredwidth/)
* class [Table](../)
* namespace [Aspose.Words.Tables](../../table/)
* assembly [Aspose.Words](../../../)
