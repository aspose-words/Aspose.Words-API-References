---
title: CellFormat
second_title: Справочник по API Aspose.Words для .NET
description: Представляет все форматирование для ячейки таблицы.
type: docs
weight: 5910
url: /ru/net/aspose.words.tables/cellformat/
---
## CellFormat class

Представляет все форматирование для ячейки таблицы.

```csharp
public class CellFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Borders](../../aspose.words.tables/cellformat/borders) { get; } | Получает набор границ ячейки. |
| [BottomPadding](../../aspose.words.tables/cellformat/bottompadding) { get; set; } | Возвращает или задает количество места (в пунктах) для добавления под содержимым ячейки. |
| [FitText](../../aspose.words.tables/cellformat/fittext) { get; set; } | Если true, текст помещается в ячейку, сжимая каждый абзац до ширины ячейки. |
| [HorizontalMerge](../../aspose.words.tables/cellformat/horizontalmerge) { get; set; } | Указывает, как ячейка объединяется по горизонтали с другими ячейками в строке. |
| [LeftPadding](../../aspose.words.tables/cellformat/leftpadding) { get; set; } | Возвращает или задает количество места (в пунктах) для добавления слева от содержимого ячейки. |
| [Orientation](../../aspose.words.tables/cellformat/orientation) { get; set; } | Возвращает или задает ориентацию текста в ячейке таблицы. |
| [PreferredWidth](../../aspose.words.tables/cellformat/preferredwidth) { get; set; } | Возвращает или задает предпочтительную ширину ячейки. |
| [RightPadding](../../aspose.words.tables/cellformat/rightpadding) { get; set; } | Возвращает или задает количество места (в пунктах) для добавления справа от содержимого ячейки. |
| [Shading](../../aspose.words.tables/cellformat/shading) { get; } | Возвращает объект Shading, который ссылается на форматирование затенения для ячейки. |
| [TopPadding](../../aspose.words.tables/cellformat/toppadding) { get; set; } | Возвращает или задает количество места (в пунктах) для добавления над содержимым ячейки. |
| [VerticalAlignment](../../aspose.words.tables/cellformat/verticalalignment) { get; set; } | Возвращает или задает вертикальное выравнивание текста в ячейке. |
| [VerticalMerge](../../aspose.words.tables/cellformat/verticalmerge) { get; set; } | Указывает, как ячейка объединяется с другими ячейками по вертикали. |
| [Width](../../aspose.words.tables/cellformat/width) { get; set; } | Получает ширину ячейки в пунктах. |
| [WrapText](../../aspose.words.tables/cellformat/wraptext) { get; set; } | Если true, перенос текста для ячейки. |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/cellformat/clearformatting)() | Восстанавливает форматирование ячейки по умолчанию. Не изменяет ширину ячейки. |
| [SetPaddings](../../aspose.words.tables/cellformat/setpaddings)(double, double, double, double) | Устанавливает количество места (в пунктах) для добавления слева/сверху/справа/снизу содержимого ячейки. |

### Примеры

Показывает, как изменить форматирование ячейки таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Установка параметров форматирования таблицы для конструктора документов
// применит их к каждой строке и ячейке, которые мы добавляем вместе с ней.
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

// Изменение форматирования применит его к текущей ячейке,
// и любые новые ячейки, которые мы впоследствии создадим с помощью конструктора.
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

Показывает, как изменить формат строк и ячеек в таблице.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Установка параметров форматирования таблицы для конструктора документов
// применит их к каждой строке и ячейке, которые мы добавляем вместе с ней.
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

// Изменение форматирования применит его к текущей ячейке,
// и любые новые ячейки, которые мы впоследствии создадим с помощью конструктора.
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

Показывает, как построить таблицу с пользовательскими границами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Установка параметров форматирования таблицы для конструктора документов
// применит их к каждой строке и ячейке, которые мы добавляем вместе с ней.
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

// Изменение форматирования применит его к текущей ячейке,
// и любые новые ячейки, которые мы впоследствии создадим с помощью конструктора.
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

* пространство имен [Aspose.Words.Tables](../../aspose.words.tables)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
