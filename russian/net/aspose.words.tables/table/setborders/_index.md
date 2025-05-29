---
title: Table.SetBorders
linktitle: SetBorders
articleTitle: SetBorders
second_title: Aspose.Words для .NET
description: С легкостью настраивайте таблицы с помощью метода SetBorders, изменяя стиль линий, ширину и цвет для придания им изысканного, профессионального вида.
type: docs
weight: 440
url: /ru/net/aspose.words.tables/table/setborders/
---
## Table.SetBorders method

Устанавливает для всех границ таблицы указанный стиль линии, ширину и цвет.

```csharp
public void SetBorders(LineStyle lineStyle, double lineWidth, Color color)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| lineStyle | LineStyle | Применяемый стиль линии. |
| lineWidth | Double | Устанавливаемая ширина линии (в пунктах). |
| color | Color | Цвет, используемый для границы. |

## Примеры

Показывает, как отформатировать все границы таблицы одновременно.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Удалить все существующие границы из таблицы.
table.ClearBorders();

// Установите одну зеленую линию, которая будет служить внешней и внутренней границей этой таблицы.
table.SetBorders(LineStyle.Single, 1.5, Color.Green);

doc.Save(ArtifactsDir + "Table.SetBorders.docx");
```

Показывает, как применять цвет границ и заливки при построении таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем таблицу и устанавливаем цвет/толщину по умолчанию для ее границ.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Создаем строку с двумя ячейками с разными цветами фона.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Сбросить форматирование ячеек, чтобы отключить цвета фона
// задаем пользовательскую толщину границы для всех новых ячеек, созданных конструктором,
// затем построим второй ряд.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### Смотрите также

* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
