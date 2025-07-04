---
title: PreferredWidth.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: Discover the PreferredWidth Type property, which defines the measurement unit for preferred width values, enhancing your design precision and flexibility.
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

Assert.That(firstCell.CellFormat.PreferredWidth.Type, Is.EqualTo(PreferredWidthType.Percent));
Assert.That(firstCell.CellFormat.PreferredWidth.Value, Is.EqualTo(11.16d));
```

### See Also

* enum [PreferredWidthType](../../preferredwidthtype/)
* class [PreferredWidth](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
