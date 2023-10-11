---
title: Class CellFormat
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Tables.CellFormat сорт. Представляет все форматирование ячейки таблицы.
type: docs
weight: 6260
url: /ru/net/aspose.words.tables/cellformat/
---
## CellFormat class

Представляет все форматирование ячейки таблицы.

Чтобы узнать больше, посетите[Работа с таблицами](https://docs.aspose.com/words/net/working-with-tables/) статья документации.

```csharp
public class CellFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Borders](../../aspose.words.tables/cellformat/borders/) { get; } | Получает коллекцию границ ячейки. |
| [BottomPadding](../../aspose.words.tables/cellformat/bottompadding/) { get; set; } | Возвращает или задает количество места (в пунктах), которое нужно добавить под содержимым ячейки. |
| [FitText](../../aspose.words.tables/cellformat/fittext/) { get; set; } | Если`истинный` , помещает текст в ячейку, сжимая каждый абзац до ширины ячейки. |
| [HideMark](../../aspose.words.tables/cellformat/hidemark/) { get; set; } |  |
| [HorizontalMerge](../../aspose.words.tables/cellformat/horizontalmerge/) { get; set; } | Указывает, как ячейка объединяется по горизонтали с другими ячейками в строке. |
| [LeftPadding](../../aspose.words.tables/cellformat/leftpadding/) { get; set; } | Возвращает или задает количество места (в пунктах), которое нужно добавить слева от содержимого ячейки. |
| [Orientation](../../aspose.words.tables/cellformat/orientation/) { get; set; } | Возвращает или задает ориентацию текста в ячейке таблицы. |
| [PreferredWidth](../../aspose.words.tables/cellformat/preferredwidth/) { get; set; } | Возвращает или устанавливает предпочтительную ширину ячейки. |
| [RightPadding](../../aspose.words.tables/cellformat/rightpadding/) { get; set; } | Возвращает или задает количество места (в пунктах), которое нужно добавить справа от содержимого ячейки. |
| [Shading](../../aspose.words.tables/cellformat/shading/) { get; } | Возвращает[`Shading`](../../aspose.words/shading/) объект, который относится к форматированию затенения ячейки. |
| [TopPadding](../../aspose.words.tables/cellformat/toppadding/) { get; set; } | Возвращает или задает количество места (в пунктах), которое нужно добавить над содержимым ячейки. |
| [VerticalAlignment](../../aspose.words.tables/cellformat/verticalalignment/) { get; set; } | Возвращает или задает вертикальное выравнивание текста в ячейке. |
| [VerticalMerge](../../aspose.words.tables/cellformat/verticalmerge/) { get; set; } | Указывает, как ячейка объединяется с другими ячейками по вертикали. |
| [Width](../../aspose.words.tables/cellformat/width/) { get; set; } | Получает ширину ячейки в пунктах. |
| [WrapText](../../aspose.words.tables/cellformat/wraptext/) { get; set; } | Если`истинный` , перенесите текст ячейки. |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/cellformat/clearformatting/)() | Сбрасывает формат ячейки по умолчанию. Не меняет ширину ячейки. |
| [SetPaddings](../../aspose.words.tables/cellformat/setpaddings/)(double, double, double, double) | Устанавливает количество места (в пунктах), добавляемое слева/сверху/справа/снизу содержимого ячейки. |

### Примеры

Показывает, как изменить форматирование ячейки таблицы.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Используйте свойство «CellFormat» ячейки, чтобы установить форматирование, изменяющее внешний вид этой ячейки.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
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

// Используйте свойство «RowFormat» первой строки, чтобы изменить форматирование
// содержимого всех ячеек в этой строке.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Используйте свойство CellFormat первой ячейки последней строки, чтобы изменить форматирование содержимого этой ячейки.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
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

* пространство имен [Aspose.Words.Tables](../../aspose.words.tables/)
* сборка [Aspose.Words](../../)


