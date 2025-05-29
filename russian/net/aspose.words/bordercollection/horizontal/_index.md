---
title: BorderCollection.Horizontal
linktitle: Horizontal
articleTitle: Horizontal
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BorderCollection Horizontal для бесшовных границ ячеек и абзацев. Улучшите свой макет с помощью идеального выравнивания и стиля!
type: docs
weight: 50
url: /ru/net/aspose.words/bordercollection/horizontal/
---
## BorderCollection.Horizontal property

Получает горизонтальную границу, которая используется между ячейками или соответствующими абзацами.

```csharp
public Border Horizontal { get; }
```

## Примеры

Показывает, как применить настройки горизонтальных границ к формату абзаца.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем красную горизонтальную границу для абзаца. Все абзацы, созданные позже, унаследуют эти настройки границ.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
borders.Horizontal.Color = Color.Red;
borders.Horizontal.LineStyle = LineStyle.DashSmallGap;
borders.Horizontal.LineWidth = 3;

// Записываем текст в документ, не создавая после этого новый абзац.
// Поскольку абзаца внизу нет, горизонтальная граница не будет видна.
builder.Write("Paragraph above horizontal border.");

// Как только мы добавим второй абзац, граница первого абзаца станет видимой.
builder.InsertParagraph();
builder.Write("Paragraph below horizontal border.");

doc.Save(ArtifactsDir + "Border.HorizontalBorders.docx");
```

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
