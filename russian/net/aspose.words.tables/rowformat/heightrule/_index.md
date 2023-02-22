---
title: RowFormat.HeightRule
second_title: Справочник по API Aspose.Words для .NET
description: RowFormat свойство. Получает или задает правило определения высоты строки таблицы.
type: docs
weight: 50
url: /ru/net/aspose.words.tables/rowformat/heightrule/
---
## RowFormat.HeightRule property

Получает или задает правило определения высоты строки таблицы.

```csharp
public HeightRule HeightRule { get; set; }
```

### Примеры

Показывает, как форматировать строки с помощью конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Начнем вторую строку, а затем настроим ее высоту. Конструктор применит эти настройки к
// его текущая строка, а также любые новые строки, которые она создает впоследствии.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// На первую строку не повлияла реконфигурация заполнения, и она по-прежнему содержит значения по умолчанию.
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

// Установите некоторые параметры форматирования для текста и внешнего вида таблицы.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// Настройка параметров форматирования в конструкторе документов применит их
// в текущую ячейку/строку, в которой находится курсор,
// а также любые новые ячейки и строки, созданные с помощью этого построителя.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Переконфигурируем объекты форматирования построителя для новых строк и ячеек, которые мы собираемся создать.
// Построитель не будет применять их к уже созданной первой строке, чтобы она выделялась как строка заголовка.
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
* пространство имен [Aspose.Words.Tables](../../rowformat/)
* сборка [Aspose.Words](../../../)


