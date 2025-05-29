---
title: Shading.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words для .NET
description: Легко удаляйте тени с ваших объектов с помощью нашего метода ClearFormatting. Улучшайте свои проекты для придания им изысканного, профессионального вида!
type: docs
weight: 80
url: /ru/net/aspose.words/shading/clearformatting/
---
## Shading.ClearFormatting method

Удаляет затенение с объекта.

```csharp
public void ClearFormatting()
```

## Примеры

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

* class [Shading](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
