---
title: Border.GetHashCode
linktitle: GetHashCode
articleTitle: GetHashCode
second_title: Aspose.Words для .NET
description: Откройте для себя метод Border GetHashCode, мощную хэш-функцию, которая повышает целостность данных и производительность ваших приложений. Раскройте его потенциал сегодня!
type: docs
weight: 110
url: /ru/net/aspose.words/border/gethashcode/
---
## Border.GetHashCode method

Служит хэш-функцией для этого типа.

```csharp
public override int GetHashCode()
```

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

* class [Border](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
