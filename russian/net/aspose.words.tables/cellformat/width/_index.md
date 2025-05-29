---
title: CellFormat.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CellFormat Width, которое позволяет легко измерить ширину ячейки в пунктах, улучшив макет и читабельность вашей электронной таблицы.
type: docs
weight: 140
url: /ru/net/aspose.words.tables/cellformat/width/
---
## CellFormat.Width property

Получает ширину ячейки в точках.

```csharp
public double Width { get; set; }
```

## Примечания

Ширина рассчитывается Aspose.Words при загрузке и сохранении документа. В настоящее время поддерживаются не все комбинации свойств таблицы, ячейки и документа. Возвращаемое значение может быть неточным для некоторых документов. Оно может не совпадать с шириной ячейки, рассчитанной MS Word при открытии документа в MS Word.

Установка этого свойства не рекомендуется. Нет гарантии, что ячейка действительно будет иметь заданную ширину. Ширина может быть скорректирована для размещения содержимого ячейки в макете таблицы с автоматическим подбором ширины. Ячейки в других строках могут иметь конфликтующие настройки ширины. Размер таблицы может быть изменен для ее размещения в контейнере или для соответствия настройкам ширины таблицы. Рассмотрите возможность использования[`PreferredWidth`](../preferredwidth/)для установки ширины ячейки. Установка этого свойства устанавливает[`PreferredWidth`](../preferredwidth/) неявно с версии 15.8.

## Примеры

Показывает, как форматировать ячейки с помощью конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Вставьте вторую ячейку, а затем настройте параметры заполнения текста ячейки.
// Конструктор применит эти настройки к текущей ячейке и ко всем новым ячейкам, которые он создаст впоследствии.
builder.InsertCell();

CellFormat cellFormat = builder.CellFormat;
cellFormat.Width = 250;
cellFormat.LeftPadding = 30;
cellFormat.RightPadding = 30;
cellFormat.TopPadding = 30;
cellFormat.BottomPadding = 30;

builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.EndTable();

// Первая ячейка не была затронута реконфигурацией заполнения и по-прежнему содержит значения по умолчанию.
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.Width);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.LeftPadding);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.RightPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.TopPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.BottomPadding);

Assert.AreEqual(250.0d, table.FirstRow.Cells[1].CellFormat.Width);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.LeftPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.RightPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.TopPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.BottomPadding);

// Первая ячейка в выходном документе все равно увеличится до размера соседней ячейки.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
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

* class [CellFormat](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
