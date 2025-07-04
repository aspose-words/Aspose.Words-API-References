---
title: HeightRule Enum
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.HeightRule enum for precise control over object height in documents. Optimize your workflow with this essential feature!
type: docs
weight: 3550
url: /net/aspose.words/heightrule/
---
## HeightRule enumeration

Specifies the rule for determining the height of an object.

```csharp
public enum HeightRule
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| AtLeast | `0` | The height will be at least the specified height in points. It will grow, if needed, to accommodate all text inside an object. |
| Exactly | `1` | The height is specified exactly in points. Please note that if the text cannot fit inside the object of this height, it will appear truncated. |
| Auto | `2` | The height will grow automatically to accommodate all text inside an object. |

## Examples

Shows how to format rows with a document builder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Start a second row, and then configure its height. The builder will apply these settings to
// its current row, as well as any new rows it creates afterwards.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// The first row was unaffected by the padding reconfiguration and still holds the default values.
Assert.That(table.Rows[0].RowFormat.Height, Is.EqualTo(0.0d));
Assert.That(table.Rows[0].RowFormat.HeightRule, Is.EqualTo(HeightRule.Auto));

Assert.That(table.Rows[1].RowFormat.Height, Is.EqualTo(100.0d));
Assert.That(table.Rows[1].RowFormat.HeightRule, Is.EqualTo(HeightRule.Exactly));

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
