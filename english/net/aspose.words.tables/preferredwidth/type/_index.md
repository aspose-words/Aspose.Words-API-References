---
title: PreferredWidth.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: PreferredWidth Type property. Gets the unit of measure used for this preferred width value in C#.
type: docs
weight: 40
url: /net/aspose.words.tables/preferredwidth/type/
---
## PreferredWidth.Type property

Gets the unit of measure used for this preferred width value.

```csharp
public PreferredWidthType Type { get; }
```

## Examples

Shows how to verify the preferred width type and value of a table cell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### See Also

* enum [PreferredWidthType](../../preferredwidthtype/)
* class [PreferredWidth](../)
* namespace [Aspose.Words.Tables](../../preferredwidth/)
* assembly [Aspose.Words](../../../)
