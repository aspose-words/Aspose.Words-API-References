---
title: Table.SetBorder
linktitle: SetBorder
articleTitle: SetBorder
second_title: Aspose.Words для .NET
description: Настройте внешний вид вашей таблицы с помощью метода SetBorder — отрегулируйте стиль линии, ширину и цвет для профессионального вида. Улучшите свой дизайн сегодня!
type: docs
weight: 430
url: /ru/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Устанавливает указанную границу таблицы на указанный стиль линии, ширину и цвет.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| borderType | BorderType | Граница таблицы, которую нужно изменить. |
| lineStyle | LineStyle | Применяемый стиль линии. |
| lineWidth | Double | Устанавливаемая ширина линии (в пунктах). |
| color | Color | Цвет, используемый для границы. |
| isOverrideCellBorders | Boolean | Когда`истинный`, приводит к удалению всех существующих явных границ ячеек. |

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

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
