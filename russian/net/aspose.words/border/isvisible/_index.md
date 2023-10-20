---
title: Border.IsVisible
linktitle: IsVisible
articleTitle: IsVisible
second_title: Aspose.Words для .NET
description: Border IsVisible свойство. Возвращаетистинный еслиLineStyle не являетсяNone  на С#.
type: docs
weight: 30
url: /ru/net/aspose.words/border/isvisible/
---
## Border.IsVisible property

Возвращает`истинный` если[`LineStyle`](../linestyle/) не являетсяNone .

```csharp
public bool IsVisible { get; }
```

## Примеры

Показывает, как удалить границы абзаца.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Каждый абзац имеет индивидуальный набор границ.
// Мы можем получить доступ к настройкам внешнего вида этих границ через объект формата абзаца.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

 // Мы можем сразу удалить границу, запустив метод ClearFormatting.
// Запуск этого метода на каждой границе абзаца удалит все его границы.
foreach (Border border in borders)
    border.ClearFormatting();

Assert.AreEqual(Color.Empty.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(0.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.None, borders[0].LineStyle);
Assert.IsFalse(borders[0].IsVisible);

doc.Save(ArtifactsDir + "Border.ClearFormatting.docx");
```

### Смотрите также

* class [Border](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
