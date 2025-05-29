---
title: Fill.FillType
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words для .NET
description: Узнайте, как эффективно задать свойство FillType и улучшить свой дизайн с помощью настраиваемых параметров заливки для лучшего визуального эффекта.
type: docs
weight: 60
url: /ru/net/aspose.words.drawing/fill/filltype/
---
## Fill.FillType property

Получает тип заполнения.

```csharp
public FillType FillType { get; }
```

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

* enum [FillType](../../filltype/)
* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
