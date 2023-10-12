---
title: DocumentBuilder.InsertCell
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Вставляет ячейку таблицы в документ.
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

### Примечания

Чтобы начать стол, просто позвоните`InsertCell` . После этого любой контент, который вы добавляете с помощью других методов[`DocumentBuilder`](../) класс будет добавлен в текущую ячейку.

Чтобы начать новую ячейку в той же строке, вызовите`InsertCell` снова.

Чтобы завершить вызов строки таблицы[`EndRow`](../endrow/).

Использовать[`CellFormat`](../cellformat/)свойство, позволяющее указать форматирование ячейки.

### Примеры

Показывает, как использовать построитель документов для создания таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Запускаем таблицу, затем заполняем первую строку двумя ячейками.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Вызов метода построителя «EndRow», чтобы начать новую строку.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Показывает, как создать таблицу с настраиваемыми границами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Установка параметров форматирования таблицы для построителя документов
// будет применять их к каждой строке и ячейке, которые мы добавляем вместе с ними.
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

// При изменении форматирования оно будет применено к текущей ячейке,
// и любые новые ячейки, которые мы создадим впоследствии с помощью построителя.
// Это не повлияет на ячейки, которые мы добавили ранее.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Увеличиваем высоту строки, чтобы она соответствовала вертикальному тексту.
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
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


