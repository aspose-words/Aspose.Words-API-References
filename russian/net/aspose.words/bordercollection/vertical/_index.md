---
title: BorderCollection.Vertical
linktitle: Vertical
articleTitle: Vertical
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BorderCollection Vertical для бесшовных границ ячеек. Улучшите свой дизайн с помощью настраиваемых вертикальных границ для изысканного вида!
type: docs
weight: 130
url: /ru/net/aspose.words/bordercollection/vertical/
---
## BorderCollection.Vertical property

Получает вертикальную границу, используемую между ячейками.

```csharp
public Border Vertical { get; }
```

## Примеры

Показывает, как применить настройки вертикальных границ к формату строки таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем таблицу с красными и синими внутренними границами.
Table table = builder.StartTable();

for (int i = 0; i < 3; i++)
{
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 1");
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 2");

    Row row = builder.EndRow();
    BorderCollection borders = row.RowFormat.Borders;

    // Настройте внешний вид границ, которые будут отображаться между строками.
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    // Настройте внешний вид границ, которые будут отображаться между ячейками.
    borders.Vertical.Color = Color.Blue;
    borders.Vertical.LineStyle = LineStyle.Dot;
    borders.Vertical.LineWidth = 2.0d;
}

// Формат строки и внутренний абзац ячейки используют разные настройки границ.
Border border = table.FirstRow.FirstCell.LastParagraph.ParagraphFormat.Borders.Vertical;

Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
Assert.AreEqual(0.0d, border.LineWidth);
Assert.AreEqual(LineStyle.None, border.LineStyle);

doc.Save(ArtifactsDir + "Border.VerticalBorders.docx");
```

### Смотрите также

* class [Border](../../border/)
* class [BorderCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
