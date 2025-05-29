---
title: Table.CellSpacing
linktitle: CellSpacing
articleTitle: CellSpacing
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Table CellSpacing, позволяющее легко настраивать интервал между ячейками в пунктах, улучшая внешний вид и читабельность таблицы.
type: docs
weight: 100
url: /ru/net/aspose.words.tables/table/cellspacing/
---
## Table.CellSpacing property

Возвращает или задает величину пространства (в пунктах) между ячейками.

```csharp
public double CellSpacing { get; set; }
```

## Примеры

Показывает, как включить интервал между отдельными ячейками в таблице.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Animal");
builder.InsertCell();
builder.Write("Class");
builder.EndRow();
builder.InsertCell();
builder.Write("Dog");
builder.InsertCell();
builder.Write("Mammal");
builder.EndTable();

table.CellSpacing = 3;

// Установите свойство «AllowCellSpacing» в значение «true», чтобы включить интервал между ячейками
// с величиной, равной значению свойства "CellSpacing" в пунктах.
// Установите свойство «AllowCellSpacing» на «false», чтобы отключить интервал между ячейками
// и игнорировать значение свойства "CellSpacing".
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// Настройка свойства «CellSpacing» автоматически включит интервал между ячейками.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

Показывает, как создать пользовательские настройки стиля для таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// Установка свойств стиля таблицы может повлиять на свойства самой таблицы.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
