---
title: Paragraph.ParentSection
linktitle: ParentSection
articleTitle: ParentSection
second_title: Aspose.Words für .NET
description: Paragraph ParentSection eigendom. Ruft das übergeordnete Element abSection des Absatzes in C#.
type: docs
weight: 200
url: /de/net/aspose.words/paragraph/parentsection/
---
## Paragraph.ParentSection property

Ruft das übergeordnete Element ab[`Section`](../../section/) des Absatzes.

```csharp
public Section ParentSection { get; }
```

## Beispiele

Zeigt, wie eine Kopf- und Fußzeile erstellt wird.

```csharp
Document doc = new Document();

// Eine Überschrift erstellen und einen Absatz daran anhängen. Der Text in diesem Absatz
// wird oben auf jeder Seite dieses Abschnitts über dem Haupttext angezeigt.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Eine Fußzeile erstellen und einen Absatz daran anhängen. Der Text in diesem Absatz
// wird unten auf jeder Seite dieses Abschnitts unter dem Haupttext angezeigt.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Siehe auch

* class [Section](../../section/)
* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
