---
title: BorderCollection.Top
linktitle: Top
articleTitle: Top
second_title: Aspose.Words для .NET
description: Откройте для себя BorderCollection, наилучшую собственность для потрясающих верхних бордюров, которые возвышают ваш дизайн. Улучшите свои проекты с помощью наших уникальных предложений!
type: docs
weight: 120
url: /ru/net/aspose.words/bordercollection/top/
---
## BorderCollection.Top property

Получает верхнюю границу.

```csharp
public Border Top { get; }
```

## Примеры

Показывает, как применять цвет границ и заливки при построении таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем таблицу и устанавливаем цвет/толщину по умолчанию для ее границ.
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

// Сбросить форматирование ячеек, чтобы отключить цвета фона
// задаем пользовательскую толщину границы для всех новых ячеек, созданных конструктором,
// затем построим второй ряд.
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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
