---
title: Fill.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words для .NET
description: Откройте для себя свойство «Цвет заливки», чтобы легко настроить цвет переднего плана вашего дизайна с помощью объекта «Цвет», повысив визуальную привлекательность вашего проекта.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing/fill/color/
---
## Fill.Color property

Возвращает или задает объект Color, представляющий цвет переднего плана для заливки.

```csharp
public Color Color { get; set; }
```

## Примечания

Это свойство сохраняет альфа-компонентуColor , в отличие от[`ForeColor`](../forecolor/) свойство, которое сбрасывает его до полностью непрозрачного цвета.

## Примеры

Показывает, как преобразовать любую заливку обратно в сплошную.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Получить объект Fill для шрифта первого прогона.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Проверьте свойства заливки шрифта.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Измените тип заливки на Сплошную с равномерным зеленым цветом.
fill.Solid();
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
