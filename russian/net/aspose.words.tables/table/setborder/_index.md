---
title: SetBorder
second_title: Справочник по API Aspose.Words для .NET
description: Устанавливает для указанной границы таблицы заданный стиль линии ширину и цвет.
type: docs
weight: 410
url: /ru/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Устанавливает для указанной границы таблицы заданный стиль линии, ширину и цвет.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| borderType | BorderType | Границу таблицы изменить. |
| lineStyle | LineStyle | Применяемый стиль линии. |
| lineWidth | Double | Задаваемая ширина линии (в пунктах). |
| color | Color | Цвет, используемый для границы. |
| isOverrideCellBorders | Boolean | Когда`истинный`, приводит к удалению всех существующих явных границ ячеек. |

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

* enum [BorderType](../../../aspose.words/bordertype)
* enum [LineStyle](../../../aspose.words/linestyle)
* class [Table](../../table)
* пространство имен [Aspose.Words.Tables](../../table)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
