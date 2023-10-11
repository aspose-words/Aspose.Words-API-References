---
title: Class Border
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Border сорт. Представляет границу объекта.
type: docs
weight: 80
url: /ru/net/aspose.words/border/
---
## Border class

Представляет границу объекта.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) статья документации.

```csharp
public class Border : InternableComplexAttr
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | Получает или задает цвет границы. |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | Получает или задает расстояние границы от текста или от края страницы в пунктах. |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | Возвращает`истинный` если[`LineStyle`](./linestyle/) не являетсяNone . |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | Получает или задает стиль границы. |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | Получает или задает ширину границы в пунктах. |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | Получает или задает значение, указывающее, имеет ли граница тень. |
| [ThemeColor](../../aspose.words/border/themecolor/) { get; set; } | Получает или задает цвет темы в примененной цветовой схеме, связанной с этим объектом Border. |
| [TintAndShade](../../aspose.words/border/tintandshade/) { get; set; } | Получает или задает двойное значение, которое осветляет или затемняет цвет. |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | Сбрасывает свойства границы к значениям по умолчанию. |
| [Equals](../../aspose.words/border/equals/#equals)(Border) | Определяет, равна ли указанная граница по значению текущей границе. |
| override [Equals](../../aspose.words/border/equals/#equals_1)(object) | Определяет, равен ли указанный объект по значению текущему объекту. |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | Служит хеш-функцией для этого типа. |

### Примечания

Границы можно применять к различным элементам документа, включая абзац, текст внутри абзаца или ячейку таблицы.

### Примеры

Показывает, как вставить в документ строку, окруженную рамкой.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

Показывает, как вставить абзац с верхней границей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Устанавливаем ThemeColor только в том случае, если установлены LineWidth или LineStyle.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Смотрите также

* class [InternableComplexAttr](../internablecomplexattr/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


