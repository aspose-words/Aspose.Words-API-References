---
title: Shading Class
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words для .NET
description: Aspose.Words.Shading сорт. Содержит атрибуты затенения для объекта на С#.
type: docs
weight: 5990
url: /ru/net/aspose.words/shading/
---
## Shading class

Содержит атрибуты затенения для объекта.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) статья документации.

```csharp
public class Shading : InternableComplexAttr
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | Получает или задает цвет, применяемый к фону`Shading` объект. |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } | Получает или задает цвет темы фонового рисунка в примененной цветовой схеме, связанной с этим`Shading` объект. |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } | Получает или задает двойное значение, которое осветляет или затемняет цвет фоновой темы. |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | Получает или задает цвет, применяемый к переднему плану`Shading` объект. |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } | Получает или задает цвет темы узора переднего плана в применяемой цветовой схеме, связанной с этим`Shading` объект. |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } | Получает или задает двойное значение, которое осветляет или затемняет цвет темы переднего плана. |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | Получает или задает текстуру затенения. |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | Удаляет затенение объекта. |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(*object*) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [Equals](../../aspose.words/shading/equals/#equals)(*Shading*) | Определяет, задано ли указанное`Shading` по значению равен текущему`Shading` . |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | Служит хеш-функцией для этого типа. |

## Примеры

Показывает, как украшать текст границами и заливкой.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

Показывает, как применять цвет границы и заливки при построении таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Запускаем таблицу и устанавливаем цвет/толщину ее границ по умолчанию.
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

// Сбрасываем форматирование ячейки, чтобы отключить цвета фона
// устанавливаем собственную толщину границы для всех новых ячеек, созданных построителем,
// затем создаем вторую строку.
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

* class [InternableComplexAttr](../internablecomplexattr/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
