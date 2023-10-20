---
title: Cell.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words для .NET
description: Cell LastParagraph свойство. Получает последний абзац среди ближайших дочерних элементов на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.tables/cell/lastparagraph/
---
## Cell.LastParagraph property

Получает последний абзац среди ближайших дочерних элементов.

```csharp
public Paragraph LastParagraph { get; }
```

## Примеры

Показывает, как применить настройки к вертикальным границам формата строки таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаём таблицу с красной и синей внутренней рамкой.
Table table = builder.StartTable();

for (int i = 0; i < 3; i++)
{
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 1");
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 2");

    Row row = builder.EndRow();
    BorderCollection borders = row.RowFormat.Borders;

    // Настраиваем внешний вид границ между строками.
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    // Настраиваем внешний вид границ между ячейками.
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
