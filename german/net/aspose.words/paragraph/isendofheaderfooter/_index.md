---
title: Paragraph.IsEndOfHeaderFooter
linktitle: IsEndOfHeaderFooter
articleTitle: IsEndOfHeaderFooter
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsEndOfHeaderFooter-Eigenschaft für Absätze. Ermitteln Sie ganz einfach, ob ein Absatz der letzte in einem HeaderFooter ist, und verbessern Sie so die Dokumentstruktur.
type: docs
weight: 70
url: /de/net/aspose.words/paragraph/isendofheaderfooter/
---
## Paragraph.IsEndOfHeaderFooter property

Wahr, wenn dieser Absatz der letzte Absatz in der[`HeaderFooter`](../../headerfooter/) (Haupttextgeschichte) eines[`Section`](../../section/) ; andernfalls false.

```csharp
public bool IsEndOfHeaderFooter { get; }
```

## Beispiele

Zeigt, wie eine Kopf- und eine Fußzeile erstellt wird.

```csharp
Document doc = new Document();

// Erstellen Sie eine Überschrift und fügen Sie einen Absatz hinzu. Der Text in diesem Absatz
// wird oben auf jeder Seite dieses Abschnitts über dem Haupttext angezeigt.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Erstellen Sie eine Fußzeile und fügen Sie einen Absatz hinzu. Der Text in diesem Absatz
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

* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
