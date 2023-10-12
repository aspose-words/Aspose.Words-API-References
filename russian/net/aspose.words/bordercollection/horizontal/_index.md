---
title: BorderCollection.Horizontal
second_title: Справочник по API Aspose.Words для .NET
description: BorderCollection свойство. Получает горизонтальную границу которая используется между ячейками или соответствующими абзацами.
type: docs
weight: 50
url: /ru/net/aspose.words/bordercollection/horizontal/
---
## BorderCollection.Horizontal property

Получает горизонтальную границу, которая используется между ячейками или соответствующими абзацами.

```csharp
public Border Horizontal { get; }
```

### Примеры

Показывает, как применить настройки к горизонтальным границам формата абзаца.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем красную горизонтальную рамку для абзаца. Любые абзацы, созданные впоследствии, унаследуют эти настройки границ.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
borders.Horizontal.Color = Color.Red;
borders.Horizontal.LineStyle = LineStyle.DashSmallGap;
borders.Horizontal.LineWidth = 3;

// Запись текста в документ без последующего создания нового абзаца.
// Поскольку внизу нет абзаца, горизонтальная граница не будет видна.
builder.Write("Paragraph above horizontal border.");

// Как только мы добавим второй абзац, граница первого абзаца станет видимой.
builder.InsertParagraph();
builder.Write("Paragraph below horizontal border.");

doc.Save(ArtifactsDir + "Border.HorizontalBorders.docx");
```

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

* class [Border](../../border/)
* class [BorderCollection](../)
* пространство имен [Aspose.Words](../../bordercollection/)
* сборка [Aspose.Words](../../../)


