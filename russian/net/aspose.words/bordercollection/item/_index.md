---
title: BorderCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BorderCollection Item для легкого доступа к объектам Border по типу. Оптимизируйте свой дизайн с помощью эффективного управления границами!
type: docs
weight: 60
url: /ru/net/aspose.words/bordercollection/item/
---
## BorderCollection indexer (1 of 2)

Извлекает[`Border`](../../border/) объект по типу границы.

```csharp
public Border this[BorderType borderType] { get; }
```

| Параметр | Описание |
| --- | --- |
| borderType | А[`BorderType`](../../bordertype/) value , который указывает тип границы для извлечения. |

## Примечания

Обратите внимание, что не все границы присутствуют для различных элементов документа. Этот метод выдает исключение, если вы запрашиваете границу, неприменимую к текущему объекту.

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

### Смотрите также

* class [Border](../../border/)
* enum [BorderType](../../bordertype/)
* class [BorderCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## BorderCollection indexer (2 of 2)

Извлекает[`Border`](../../border/) объект по индексу.

```csharp
public Border this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Отсчитываемый от нуля индекс границы, которую необходимо получить. |

## Примеры

Показывает, как коллекции границ могут совместно использовать элементы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// Поскольку мы использовали ту же конфигурацию границ при создании
// эти абзацы и их коллекции границ имеют одни и те же элементы.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
BorderCollection secondParagraphBorders = builder.CurrentParagraph.ParagraphFormat.Borders;
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsTrue(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());
    Assert.False(firstParagraphBorders[i].IsVisible);
}

foreach (Border border in secondParagraphBorders)
    border.LineStyle = LineStyle.DotDash;

// После изменения стиля линий границ только во втором абзаце,
// коллекции границ больше не содержат одни и те же элементы.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // Изменение внешнего вида пустой границы делает ее видимой.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### Смотрите также

* class [Border](../../border/)
* class [BorderCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
