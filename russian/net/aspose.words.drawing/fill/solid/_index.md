---
title: Fill.Solid
linktitle: Solid
articleTitle: Solid
second_title: Aspose.Words для .NET
description: Fill Solid метод. Устанавливает однородный цвет заливки на С#.
type: docs
weight: 250
url: /ru/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Устанавливает однородный цвет заливки.

```csharp
public void Solid()
```

## Примечания

Используйте этот метод, чтобы преобразовать любую заливку обратно в сплошную заливку.

### Смотрите также

* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)

---

## Solid(*Color*) {#solid_1}

Устанавливает заливку заданного однородного цвета.

```csharp
public void Solid(Color color)
```

## Примечания

Используйте этот метод, чтобы преобразовать любую заливку обратно в сплошную заливку.

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
