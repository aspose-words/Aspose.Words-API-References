---
title: Table.SetShading
second_title: Справочник по API Aspose.Words для .NET
description: Table метод. Устанавливает затенение на указанные значения для всей таблицы.
type: docs
weight: 450
url: /ru/net/aspose.words.tables/table/setshading/
---
## Table.SetShading method

Устанавливает затенение на указанные значения для всей таблицы.

```csharp
public void SetShading(TextureIndex texture, Color foregroundColor, Color backgroundColor)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| texture | TextureIndex | Текстура для нанесения. |
| foregroundColor | Color | Цвет текстуры. |
| backgroundColor | Color | Цвет заливки фона. |

### Примеры

Показывает, как применить контурную рамку к таблице.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Выравниваем таблицу по центру страницы.
table.Alignment = TableAlignment.Center;

// Очистим все существующие границы и затенение таблицы.
table.ClearBorders();
table.ClearShading();

// Добавляем зеленые рамки к контуру таблицы.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Заполняем ячейки светло-зеленым сплошным цветом.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Смотрите также

* enum [TextureIndex](../../../aspose.words/textureindex/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../table/)
* сборка [Aspose.Words](../../../)


