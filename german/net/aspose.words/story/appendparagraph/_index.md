---
title: Story.AppendParagraph
linktitle: AppendParagraph
articleTitle: AppendParagraph
second_title: Aspose.Words für .NET
description: Entdecken Sie die Story AppendParagraph-Methode, erstellen und hängen Sie mühelos ein Absatzobjekt mit anpassbarem Text an, um Dokumente nahtlos zu verbessern.
type: docs
weight: 60
url: /de/net/aspose.words/story/appendparagraph/
---
## Story.AppendParagraph method

Eine Abkürzungsmethode, die eine[`Paragraph`](../../paragraph/) Objekt mit optionalem Text und hängt ihn an das Ende dieses Objekts an.

```csharp
public Paragraph AppendParagraph(string text)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| text | String | Der Text für den Absatz. Kann sein`null` oder eine leere Zeichenfolge. |

### Rückgabewert

Der neu erstellte und angehängte Absatz.

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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
