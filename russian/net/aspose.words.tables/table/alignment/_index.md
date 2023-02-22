---
title: Table.Alignment
second_title: Справочник по API Aspose.Words для .NET
description: Table свойство. Указывает как встроенная таблица выравнивается в документе.
type: docs
weight: 40
url: /ru/net/aspose.words.tables/table/alignment/
---
## Table.Alignment property

Указывает, как встроенная таблица выравнивается в документе.

```csharp
public TableAlignment Alignment { get; set; }
```

### Примечания

Значение по умолчаниюLeft.

### Примеры

Показывает, как применить границу контура к таблице.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Выравниваем таблицу по центру страницы.
table.Alignment = TableAlignment.Center;

// Очистить все существующие границы и затенение из таблицы.
table.ClearBorders();
table.ClearShading();

// Добавляем зеленые рамки к контуру таблицы.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Заливаем ячейки светло-зеленым сплошным цветом.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Смотрите также

* enum [TableAlignment](../../tablealignment/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../table/)
* сборка [Aspose.Words](../../../)


