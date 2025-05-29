---
title: Table.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words для .NET
description: Откройте для себя свойство «Выравнивание таблиц», которое позволит вам легко управлять расположением встроенных таблиц в документах и придавать им изысканный профессиональный вид.
type: docs
weight: 40
url: /ru/net/aspose.words.tables/table/alignment/
---
## Table.Alignment property

Указывает, как встроенная таблица выравнивается в документе.

```csharp
public TableAlignment Alignment { get; set; }
```

## Примечания

Значение по умолчанию:Left.

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

### Смотрите также

* enum [TableAlignment](../../tablealignment/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
