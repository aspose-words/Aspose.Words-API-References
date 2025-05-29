---
title: Table.SetShading
linktitle: SetShading
articleTitle: SetShading
second_title: Aspose.Words для .NET
description: Улучшите внешний вид вашего стола с помощью метода SetShading, который позволяет применять пользовательские значения затенения для придания ему изысканного, профессионального вида.
type: docs
weight: 450
url: /ru/net/aspose.words.tables/table/setshading/
---
## Table.SetShading method

Устанавливает затенение для указанных значений по всей таблице.

```csharp
public void SetShading(TextureIndex texture, Color foregroundColor, Color backgroundColor)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| texture | TextureIndex | Применяемая текстура. |
| foregroundColor | Color | Цвет текстуры. |
| backgroundColor | Color | Цвет фоновой заливки. |

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

* enum [TextureIndex](../../../aspose.words/textureindex/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
