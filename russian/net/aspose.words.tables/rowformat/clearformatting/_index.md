---
title: RowFormat.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words для .NET
description: Узнайте, как метод RowFormat ClearFormatting без труда восстанавливает стиль данных по умолчанию, повышая ясность и наглядность.
type: docs
weight: 60
url: /ru/net/aspose.words.tables/rowformat/clearformatting/
---
## RowFormat.ClearFormatting method

Сбрасывает форматирование строк до значения по умолчанию.

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

* class [RowFormat](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
