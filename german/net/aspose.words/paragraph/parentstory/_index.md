---
title: Paragraph.ParentStory
second_title: Aspose.Words für .NET-API-Referenz
description: Paragraph eigendom. Ruft die möglicherweise übergeordnete Story auf Abschnittsebene abBody oderHeaderFooter .
type: docs
weight: 210
url: /de/net/aspose.words/paragraph/parentstory/
---
## Paragraph.ParentStory property

Ruft die möglicherweise übergeordnete Story auf Abschnittsebene ab[`Body`](../../body/) oder[`HeaderFooter`](../../headerfooter/) .

```csharp
public Story ParentStory { get; }
```

### Beispiele

Zeigt, wie Sie eine Kopf- und eine Fußzeile erstellen.

```csharp
Document doc = new Document();

// Erstellen Sie eine Kopfzeile und hängen Sie einen Absatz daran an. Der Text in diesem Absatz
// erscheint oben auf jeder Seite dieses Abschnitts über dem Haupttext.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Erstellen Sie eine Fußzeile und hängen Sie einen Absatz daran an. Der Text in diesem Absatz
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

* class [Story](../../story/)
* class [Paragraph](../)
* namensraum [Aspose.Words](../../paragraph/)
* Montage [Aspose.Words](../../../)


