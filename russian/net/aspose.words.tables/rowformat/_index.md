---
title: RowFormat Class
linktitle: RowFormat
articleTitle: RowFormat
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Tables.RowFormat для комплексного форматирования строк таблиц. Улучшите дизайн документа с помощью мощных, гибких функций.
type: docs
weight: 7180
url: /ru/net/aspose.words.tables/rowformat/
---
## RowFormat class

Представляет все форматирование для строки таблицы.

Чтобы узнать больше, посетите[Работа с таблицами](https://docs.aspose.com/words/net/working-with-tables/) документальная статья.

```csharp
public class RowFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AllowBreakAcrossPages](../../aspose.words.tables/rowformat/allowbreakacrosspages/) { get; set; } | Истинно, если текст в строке таблицы может быть разделен на разрыв страницы. |
| [Borders](../../aspose.words.tables/rowformat/borders/) { get; } | Получает коллекцию границ ячеек по умолчанию для строки. |
| [HeadingFormat](../../aspose.words.tables/rowformat/headingformat/) { get; set; } | Истина, если строка повторяется как заголовок таблицы на каждой странице, когда таблица занимает более одной страницы. |
| [Height](../../aspose.words.tables/rowformat/height/) { get; set; } | Возвращает или задает высоту строки таблицы в пунктах. |
| [HeightRule](../../aspose.words.tables/rowformat/heightrule/) { get; set; } | Возвращает или задает правило определения высоты строки таблицы. |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/rowformat/clearformatting/)() | Сбрасывает форматирование строк до значения по умолчанию. |

## Примеры

Показывает, как изменить форматирование строки таблицы.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Используйте свойство "RowFormat" первой строки, чтобы задать форматирование, которое изменяет внешний вид всей строки.
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
```

Показывает, как изменить формат строк и ячеек в таблице.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// Используйте свойство "RowFormat" первой строки для изменения форматирования
// содержимого всех ячеек в этой строке.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Используйте свойство «CellFormat» первой ячейки в последней строке, чтобы изменить форматирование содержимого этой ячейки.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
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

* пространство имен [Aspose.Words.Tables](../../aspose.words.tables/)
* сборка [Aspose.Words](../../)
