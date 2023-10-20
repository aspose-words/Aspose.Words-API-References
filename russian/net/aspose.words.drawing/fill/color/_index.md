---
title: Fill.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words для .NET
description: Fill Color свойство. Получает или задает объект Color который представляет цвет переднего плана для заливки на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.drawing/fill/color/
---
## Fill.Color property

Получает или задает объект Color, который представляет цвет переднего плана для заливки.

```csharp
public Color Color { get; set; }
```

## Примечания

Это свойство сохраняет альфа-компонентColor , в отличие от[`ForeColor`](../forecolor/)свойство, которое сбрасывает его до полностью непрозрачного цвета.

## Примеры

Показывает, как преобразовать любую заливку обратно в сплошную заливку.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Получаем объект Fill для шрифта первого запуска.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Проверяем свойства заливки шрифта.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Изменяем тип заливки на Сплошную с однородным зеленым цветом.
fill.Solid(Color.Green);
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Смотрите также

* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
