---
title: PreferredWidthType Enum
linktitle: PreferredWidthType
articleTitle: PreferredWidthType
second_title: Aspose.Words for .NET
description: Aspose.Words.Tables.PreferredWidthType enum. Specifies the unit of measurement for the preferred width of a table or cell in C#.
type: docs
weight: 6320
url: /net/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enumeration

Specifies the unit of measurement for the preferred width of a table or cell.

```csharp
public enum PreferredWidthType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Auto | `1` | The preferred width is not specified. The actual width of the table or cell is either specified using the explicit width or will be determined automatically by the table layout algorithm when the table is displayed, depending on the table auto fit setting. |
| Percent | `2` | Measure the current item width using a specified percentage. |
| Points | `3` | Measure the current item width using a specified number of points (1/72 inch). |

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

* class [PreferredWidth](../preferredwidth/)
* namespace [Aspose.Words.Tables](../../aspose.words.tables/)
* assembly [Aspose.Words](../../)
