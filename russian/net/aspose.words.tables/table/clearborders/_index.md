---
title: Table.ClearBorders
linktitle: ClearBorders
articleTitle: ClearBorders
second_title: Aspose.Words для .NET
description: Откройте для себя метод Table ClearBorders, который позволит без труда удалить все границы таблиц и ячеек, повысив ясность и привлекательность вашего дизайна.
type: docs
weight: 390
url: /ru/net/aspose.words.tables/table/clearborders/
---
## Table.ClearBorders method

Удаляет все границы таблиц и ячеек в этой таблице.

```csharp
public void ClearBorders()
```

## Примеры

Показывает, как применить контурную рамку к таблице.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Выровняйте таблицу по центру страницы.
table.Alignment = TableAlignment.Center;

// Удалим все существующие границы и заливку из таблицы.
table.ClearBorders();
table.ClearShading();

// Добавляем зеленые границы к контуру таблицы.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Заполните ячейки светло-зеленым сплошным цветом.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

Показывает, как удалить все границы из таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

// Измените цвет и толщину верхней границы.
Border topBorder = table.FirstRow.RowFormat.Borders[BorderType.Top];
table.SetBorder(BorderType.Top, LineStyle.Double, 1.5, Color.Red, true);

Assert.AreEqual(1.5d, topBorder.LineWidth);
Assert.AreEqual(Color.Red.ToArgb(), topBorder.Color.ToArgb());
Assert.AreEqual(LineStyle.Double, topBorder.LineStyle);

// Очищаем границы всех ячеек таблицы, а затем сохраняем документ.
table.ClearBorders();
doc.Save(ArtifactsDir + "Table.ClearBorders.docx");

// Проверяем значения свойств таблицы после повторного открытия документа.
doc = new Document(ArtifactsDir + "Table.ClearBorders.docx");
table = doc.FirstSection.Body.Tables[0];
topBorder = table.FirstRow.RowFormat.Borders[BorderType.Top];

Assert.AreEqual(0.0d, topBorder.LineWidth);
Assert.AreEqual(Color.Empty.ToArgb(), topBorder.Color.ToArgb());
Assert.AreEqual(LineStyle.None, topBorder.LineStyle);
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
