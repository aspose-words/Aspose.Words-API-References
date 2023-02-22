---
title: BorderCollection.ClearFormatting
second_title: Справочник по API Aspose.Words для .NET
description: BorderCollection метод. Удаляет все границы объекта.
type: docs
weight: 140
url: /ru/net/aspose.words/bordercollection/clearformatting/
---
## BorderCollection.ClearFormatting method

Удаляет все границы объекта.

```csharp
public void ClearFormatting()
```

### Примеры

Показывает, как удалить все границы из всех абзацев в документе.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Первый абзац этого документа имеет видимые границы с этими настройками.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), firstParagraphBorders.Color.ToArgb());
Assert.AreEqual(LineStyle.Single, firstParagraphBorders.LineStyle);
Assert.AreEqual(3.0d, firstParagraphBorders.LineWidth);

// Используйте метод ClearFormatting для каждого абзаца, чтобы удалить все границы.
foreach (Paragraph paragraph in doc.FirstSection.Body.Paragraphs)
{
    paragraph.ParagraphFormat.Borders.ClearFormatting();

    foreach (Border border in paragraph.ParagraphFormat.Borders)
    {
        Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
        Assert.AreEqual(LineStyle.None, border.LineStyle);
        Assert.AreEqual(0.0d, border.LineWidth);
    }
}

doc.Save(ArtifactsDir + "BorderCollection.RemoveAllBorders.docx");
```

### Смотрите также

* class [BorderCollection](../)
* пространство имен [Aspose.Words](../../bordercollection/)
* сборка [Aspose.Words](../../../)


