---
title: Fill.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words для .NET
description: Отрегулируйте прозрачность заливки от 0,0 (непрозрачная) до 1,0 (прозрачная) для настраиваемых визуальных эффектов в ваших проектах. Улучшите эстетику вашего проекта сегодня!
type: docs
weight: 200
url: /ru/net/aspose.words.drawing/fill/transparency/
---
## Fill.Transparency property

Возвращает или задает степень прозрачности указанной заливки в виде значения от 0,0 (непрозрачная) до 1,0 (прозрачная).

```csharp
public double Transparency { get; set; }
```

## Примечания

Это свойство является противоположностью свойства[`Opacity`](../opacity/).

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
