---
title: Table.ConvertToHorizontallyMergedCells
linktitle: ConvertToHorizontallyMergedCells
articleTitle: ConvertToHorizontallyMergedCells
second_title: Aspose.Words для .NET
description: Table ConvertToHorizontallyMergedCells метод. Преобразует ячейки объединенные горизонтально по ширине в ячейки объединенные по ширине.HorizontalMerge  на С#.
type: docs
weight: 390
url: /ru/net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

Преобразует ячейки, объединенные горизонтально по ширине, в ячейки, объединенные по ширине.[`HorizontalMerge`](../../cellformat/horizontalmerge/) .

```csharp
public void ConvertToHorizontallyMergedCells()
```

## Примечания

Ячейки таблицы можно объединить горизонтально либо с помощью флагов слияния.[`HorizontalMerge`](../../cellformat/horizontalmerge/) или используя ширину ячейки[`Width`](../../cellformat/width/).

Когда ячейка таблицы объединяется по свойству ширины[`HorizontalMerge`](../../cellformat/horizontalmerge/) бессмысленно, но иногда использование флагов слияния является более удобным способом.

Используйте этот метод для преобразования ячеек таблицы, объединенных горизонтально по ширине, в ячейки, объединенные флагами слияния.

## Примеры

Показывает, как преобразовать ячейки, объединенные горизонтально по ширине, в ячейки, объединенные с помощью CellFormat.HorizontalMerge.

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// Microsoft Word больше не записывает флаги слияния, вместо этого определяя объединенные ячейки по ширине.
// Aspose.Words по умолчанию определяет только 5 ячеек подряд, и ни одна из них не имеет флага горизонтального слияния,
// хотя до горизонтального слияния в строке было 7 ячеек.
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.AreEqual(5, row.Cells.Count);
Assert.True(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None));

// Используйте метод «ConvertToHorizontallyMergedCells» для преобразования ячеек, объединенных по горизонтали
// по ширине к ячейке, горизонтально объединенной флагами.
// Теперь у нас есть 7 ячеек, и некоторые из них имеют значения горизонтального слияния.
table.ConvertToHorizontallyMergedCells();
row = table.Rows[0];

Assert.AreEqual(7, row.Cells.Count);

Assert.AreEqual(CellMerge.None, row.Cells[0].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.First, row.Cells[1].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.Previous, row.Cells[2].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.None, row.Cells[3].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.First, row.Cells[4].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.Previous, row.Cells[5].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.None, row.Cells[6].CellFormat.HorizontalMerge);
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
