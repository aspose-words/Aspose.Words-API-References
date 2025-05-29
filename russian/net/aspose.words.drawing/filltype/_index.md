---
title: FillType Enum
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.FillType, чтобы улучшить ваши заполняемые объекты с помощью универсальных типов заливки для улучшения дизайна документа.
type: docs
weight: 1280
url: /ru/net/aspose.words.drawing/filltype/
---
## FillType enumeration

Указывает тип заливки для заполняемого объекта.

```csharp
public enum FillType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Solid | `1` | Сплошная заливка. |
| Patterned | `2` | Узорчатая заливка. |
| Gradient | `3` | Градиентная заливка. |
| Textured | `4` | Текстурированная заливка. |
| Background | `5` | Заливка такая же, как у фона. |
| Picture | `6` | Заполнение изображения. |

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

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
