---
title: RowFormat.HeightRule
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words для .NET
description: Откройте для себя свойство RowFormat HeightRule, чтобы легко настраивать высоту строк таблицы для оптимальной компоновки и дизайна в ваших приложениях.
type: docs
weight: 50
url: /ru/net/aspose.words.tables/rowformat/heightrule/
---
## RowFormat.HeightRule property

Возвращает или задает правило определения высоты строки таблицы.

```csharp
public HeightRule HeightRule { get; set; }
```

## Примеры

Показывает, как форматировать строки с помощью конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Начните вторую строку, а затем настройте ее высоту. Строитель применит эти настройки к
// его текущая строка, а также любые новые строки, которые он создаст впоследствии.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// Первая строка не была затронута реконфигурацией заполнения и по-прежнему содержит значения по умолчанию.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

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

* enum [HeightRule](../../../aspose.words/heightrule/)
* class [RowFormat](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
