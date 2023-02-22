---
title: BorderCollection.Right
second_title: Справочник по API Aspose.Words для .NET
description: BorderCollection свойство. Получает правильную границу.
type: docs
weight: 100
url: /ru/net/aspose.words/bordercollection/right/
---
## BorderCollection.Right property

Получает правильную границу.

```csharp
public Border Right { get; }
```

### Примеры

Показывает, как применить цвет рамки и заливки при построении таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Запускаем таблицу и устанавливаем для ее границ цвет/толщину по умолчанию.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Создаем строку с двумя ячейками с разными цветами фона.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Сбросить форматирование ячейки, чтобы отключить цвета фона
// установить пользовательскую толщину границы для всех новых ячеек, созданных конструктором,
// затем построить вторую строку.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### Смотрите также

* class [Border](../../border/)
* class [BorderCollection](../)
* пространство имен [Aspose.Words](../../bordercollection/)
* сборка [Aspose.Words](../../../)


