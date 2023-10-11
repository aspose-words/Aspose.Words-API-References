---
title: ParagraphFormat.PageBreakBefore
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Истинно если перед абзацем принудительно устанавливается разрыв страницы.
type: docs
weight: 260
url: /ru/net/aspose.words/paragraphformat/pagebreakbefore/
---
## ParagraphFormat.PageBreakBefore property

Истинно, если перед абзацем принудительно устанавливается разрыв страницы.

```csharp
public bool PageBreakBefore { get; set; }
```

### Примеры

Показывает, как создавать абзацы с разрывами страниц в начале.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Установите этот флаг в значение «истина», чтобы применить разрыв страницы к началу каждого абзаца.
// который создатель документа создаст в этой конфигурации ParagraphFormat.
// Первый абзац не получит разрыв страницы.
// Оставьте этот флаг равным «false», чтобы каждый новый абзац начинался на той же странице.
// как и предыдущий, при условии, что достаточно места.
builder.ParagraphFormat.PageBreakBefore = pageBreakBefore;

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

LayoutCollector layoutCollector = new LayoutCollector(doc);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

if (pageBreakBefore)
{
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[0]));
    Assert.AreEqual(2, layoutCollector.GetStartPageIndex(paragraphs[1]));
}
else
{
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[0]));
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[1]));
}

doc.Save(ArtifactsDir + "ParagraphFormat.PageBreakBefore.docx");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


