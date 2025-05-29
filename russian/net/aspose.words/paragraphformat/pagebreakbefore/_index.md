---
title: ParagraphFormat.PageBreakBefore
linktitle: PageBreakBefore
articleTitle: PageBreakBefore
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ParagraphFormat PageBreakBefore, с легкостью управляйте разрывами страниц перед абзацами для улучшенного форматирования и удобства чтения документа.
type: docs
weight: 270
url: /ru/net/aspose.words/paragraphformat/pagebreakbefore/
---
## ParagraphFormat.PageBreakBefore property

Истинно, если разрыв страницы принудительно вставлен перед абзацем.

```csharp
public bool PageBreakBefore { get; set; }
```

## Примеры

Показывает, как создавать абзацы с разрывами страниц в начале.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Установите этот флаг в значение «true», чтобы применить разрыв страницы к началу каждого абзаца
// который создаст конструктор документов в рамках этой конфигурации ParagraphFormat.
// Первый абзац не будет иметь разрыва страницы.
// Оставьте этот флаг как «false», чтобы начинать каждый новый абзац на той же странице
// как и в предыдущем случае, при условии наличия достаточного места.
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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
