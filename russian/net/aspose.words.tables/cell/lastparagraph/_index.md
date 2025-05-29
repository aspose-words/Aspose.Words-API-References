---
title: Cell.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Cell LastParagraph. Легко получайте доступ к последнему абзацу из непосредственных дочерних элементов для эффективного управления контентом.
type: docs
weight: 60
url: /ru/net/aspose.words.tables/cell/lastparagraph/
---
## Cell.LastParagraph property

Получает последний абзац среди непосредственных дочерних элементов.

```csharp
public Paragraph LastParagraph { get; }
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Cell](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
