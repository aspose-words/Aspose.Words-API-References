---
title: Table.SetBorder
linktitle: SetBorder
articleTitle: SetBorder
second_title: Aspose.Words для .NET
description: Table SetBorder метод. Устанавливает указанную границу таблицы с указанным стилем шириной и цветом линии на С#.
type: docs
weight: 410
url: /ru/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Устанавливает указанную границу таблицы с указанным стилем, шириной и цветом линии.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| borderType | BorderType | Граница таблицы, которую необходимо изменить. |
| lineStyle | LineStyle | Применяемый стиль линии. |
| lineWidth | Double | Толщина линии, которую необходимо установить (в пунктах). |
| color | Color | Цвет, используемый для границы. |
| isOverrideCellBorders | Boolean | Когда`истинный`, приводит к удалению всех существующих явных границ ячеек. |

## Примеры

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

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
