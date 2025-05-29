---
title: DocumentBuilder.InsertCell
linktitle: InsertCell
articleTitle: InsertCell
second_title: Aspose.Words для .NET
description: Легко улучшайте свои документы с помощью метода InsertCell в DocumentBuilder — быстро добавляйте настраиваемые ячейки таблиц для лучшей организации и ясности.
type: docs
weight: 270
url: /ru/net/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder.InsertCell method

Вставляет ячейку таблицы в документ.

```csharp
public Cell InsertCell()
```

### Возвращаемое значение

Узел ячейки, который был только что вставлен.

## Примечания

Чтобы начать игру за столом, просто позвоните`InsertCell` . После этого любой контент, который вы добавляете с помощью других методов[`DocumentBuilder`](../) класс будет добавлен в текущую ячейку.

Чтобы начать новую ячейку в той же строке, вызовите`InsertCell` снова.

Чтобы завершить вызов строки таблицы[`EndRow`](../endrow/).

Используйте[`CellFormat`](../cellformat/) свойство для указания форматирования ячеек.

## Примеры

Показывает, как использовать конструктор документов для создания таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Запускаем таблицу, затем заполняем первую строку двумя ячейками.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Вызываем метод «EndRow» конструктора, чтобы начать новую строку.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Показывает, как создать таблицу с пользовательскими границами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Настройка параметров форматирования таблиц для конструктора документов
// применит их к каждой строке и ячейке, которые мы добавим вместе с ним.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// Изменение форматирования применится к текущей ячейке,
// и любые новые ячейки, которые мы создадим с помощью конструктора впоследствии.
// Это не повлияет на ячейки, которые мы добавили ранее.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Увеличиваем высоту строки, чтобы вместить вертикальный текст.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Смотрите также

* class [Cell](../../../aspose.words.tables/cell/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
