---
title: BorderCollection Class
linktitle: BorderCollection
articleTitle: BorderCollection
second_title: Aspose.Words для .NET
description: Aspose.Words.BorderCollection сорт. КоллекцияBorder объекты на С#.
type: docs
weight: 90
url: /ru/net/aspose.words/bordercollection/
---
## BorderCollection class

Коллекция[`Border`](../border/) объекты.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) статья документации.

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | Получает нижнюю границу. |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | Получает или задает цвет границы. |
| [Count](../../aspose.words/bordercollection/count/) { get; } | Получает количество границ в коллекции. |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | Получает или задает расстояние границы от текста в пунктах. |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | Получает горизонтальную границу, которая используется между ячейками или соответствующими абзацами. |
| [Item](../../aspose.words/bordercollection/item/) { get; } | Получает[`Border`](../border/) объект по типу границы. (2 indexers) |
| [Left](../../aspose.words/bordercollection/left/) { get; } | Получает левую границу. |
| [LineStyle](../../aspose.words/bordercollection/linestyle/) { get; set; } | Получает или задает стиль границы. |
| [LineWidth](../../aspose.words/bordercollection/linewidth/) { get; set; } | Получает или задает ширину границы в пунктах. |
| [Right](../../aspose.words/bordercollection/right/) { get; } | Получает правую границу. |
| [Shadow](../../aspose.words/bordercollection/shadow/) { get; set; } | Получает или задает значение, указывающее, имеет ли граница тень. |
| [Top](../../aspose.words/bordercollection/top/) { get; } | Получает верхнюю границу. |
| [Vertical](../../aspose.words/bordercollection/vertical/) { get; } | Получает вертикальную границу, которая используется между ячейками. |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormatting](../../aspose.words/bordercollection/clearformatting/)() | Удаляет все границы объекта. |
| [Equals](../../aspose.words/bordercollection/equals/#equals)(*BorderCollection*) | Сравнивает коллекции границ. |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для обхода всех границ коллекции. |

## Примечания

Разные элементы документа имеют разные границы. Например,[`ParagraphFormat`](../paragraphformat/)имеет[`Bottom`](./bottom/) ,[`Left`](./left/) ,[`Right`](./right/) и[`Top`](./top/) borders. Вы можете указать различное форматирование для каждой границы независимо или перечислить все границы и применить одинаковое форматирование.

## Примеры

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

* class [Border](../border/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
