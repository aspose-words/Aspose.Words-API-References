---
title: Table.LeftIndent
linktitle: LeftIndent
articleTitle: LeftIndent
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Table LeftIndent, чтобы легко настроить левый отступ вашей таблицы. Улучшите свой дизайн с помощью точного управления для лучших макетов!
type: docs
weight: 190
url: /ru/net/aspose.words.tables/table/leftindent/
---
## Table.LeftIndent property

Возвращает или задает значение, представляющее левый отступ таблицы.

```csharp
public double LeftIndent { get; set; }
```

## Примеры

Показывает, как создать форматированную таблицу с помощью DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// Задайте некоторые параметры форматирования для внешнего вида текста и таблицы.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// Настройка параметров форматирования в конструкторе документов применит их
// к текущей ячейке/строке, в которой находится курсор,
// а также любые новые ячейки и строки, созданные с помощью этого конструктора.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Перенастраиваем объекты форматирования конструктора для новых строк и ячеек, которые мы собираемся создать.
// Конструктор не будет применять их к первой уже созданной строке, поэтому она будет выделяться как строка заголовка.
builder.CellFormat.Shading.BackgroundPatternColor = Color.White;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.RowFormat.Height = 30;
builder.RowFormat.HeightRule = HeightRule.Auto;
builder.InsertCell();
builder.Font.Size = 12;
builder.Font.Bold = false;

builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");
builder.InsertCell();
builder.Write("Row 1, Cell 3.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.InsertCell();
builder.Write("Row 2, Cell 3.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateFormattedTable.docx");
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
