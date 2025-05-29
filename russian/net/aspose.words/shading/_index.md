---
title: Shading Class
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Shading, разработанный для улучшения ваших документов с помощью настраиваемых атрибутов затенения для придания им профессионального вида.
type: docs
weight: 6820
url: /ru/net/aspose.words/shading/
---
## Shading class

Содержит атрибуты затенения для объекта.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) документальная статья.

```csharp
public class Shading : InternableComplexAttr
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | Возвращает или задает цвет, применяемый к фону`Shading` объект. |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } | Возвращает или задает цвет темы фонового узора в примененной цветовой схеме, связанной с этим`Shading` объект. |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } | Возвращает или задает двойное значение, которое осветляет или затемняет цвет фоновой темы. |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | Возвращает или задает цвет, применяемый к переднему плану`Shading` объект. |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } | Возвращает или задает цвет темы узора переднего плана в примененной цветовой схеме, которая связана с этим`Shading` объект. |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } | Возвращает или задает двойное значение, которое осветляет или затемняет цвет темы переднего плана. |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | Получает или задает текстуру затенения. |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | Удаляет затенение с объекта. |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(*object*) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [Equals](../../aspose.words/shading/equals/#equals)(*Shading*) | Определяет, является ли указанный`Shading` равен по значению текущему`Shading` . |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | Служит хэш-функцией для этого типа. |

## Примеры

Показывает, как оформить текст с помощью границ и заливки.

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

* class [InternableComplexAttr](../internablecomplexattr/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
