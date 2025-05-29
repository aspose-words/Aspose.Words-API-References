---
title: Font.Fill
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words для .NET
description: Откройте для себя свойство «Заливка шрифта», чтобы улучшить внешний вид текста с помощью настраиваемого форматирования заливки для придания ему изысканного, профессионального вида.
type: docs
weight: 130
url: /ru/net/aspose.words/font/fill/
---
## Font.Fill property

Получает форматирование заполнения для[`Font`](../) .

```csharp
public Fill Fill { get; }
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

* class [Fill](../../../aspose.words.drawing/fill/)
* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
