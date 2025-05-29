---
title: BorderCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words для .NET
description: Узнайте, как метод BorderCollection ClearFormatting без труда удаляет все границы объектов, улучшая ваш дизайн с помощью чистых и четких визуальных эффектов.
type: docs
weight: 140
url: /ru/net/aspose.words/bordercollection/clearformatting/
---
## BorderCollection.ClearFormatting method

Удаляет все границы объекта.

```csharp
public void ClearFormatting()
```

## Примеры

Показывает, как удалить все границы из всех абзацев в документе.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Первый абзац этого документа имеет видимые границы с этими настройками.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), firstParagraphBorders.Color.ToArgb());
Assert.AreEqual(LineStyle.Single, firstParagraphBorders.LineStyle);
Assert.AreEqual(3.0d, firstParagraphBorders.LineWidth);

// Используйте метод «ClearFormatting» для каждого абзаца, чтобы удалить все границы.
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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
