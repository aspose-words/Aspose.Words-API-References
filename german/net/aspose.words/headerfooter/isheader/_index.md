---
title: HeaderFooter.IsHeader
second_title: Aspose.Words für .NET-API-Referenz
description: HeaderFooter eigendom. Wahr wenn dies der Fall ist Kopfzeile Fußzeile Objekt ist ein Header.
type: docs
weight: 30
url: /de/net/aspose.words/headerfooter/isheader/
---
## HeaderFooter.IsHeader property

Wahr, wenn dies der Fall ist **Kopfzeile Fußzeile** Objekt ist ein Header.

```csharp
public bool IsHeader { get; }
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

* class [HeaderFooter](../)
* namensraum [Aspose.Words](../../headerfooter/)
* Montage [Aspose.Words](../../../)


