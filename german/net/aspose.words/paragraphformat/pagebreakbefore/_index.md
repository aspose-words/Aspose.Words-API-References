---
title: ParagraphFormat.PageBreakBefore
second_title: Aspose.Words für .NET-API-Referenz
description: ParagraphFormat eigendom. True wenn vor dem Absatz ein Seitenumbruch erzwungen wird.
type: docs
weight: 260
url: /de/net/aspose.words/paragraphformat/pagebreakbefore/
---
## ParagraphFormat.PageBreakBefore property

True, wenn vor dem Absatz ein Seitenumbruch erzwungen wird.

```csharp
public bool PageBreakBefore { get; set; }
```

### Beispiele

Zeigt, wie Absätze mit Seitenumbrüchen am Anfang erstellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Setzen Sie dieses Flag auf „true“, um am Anfang jedes Absatzes einen Seitenumbruch anzuwenden
// dass der Dokumentersteller unter dieser ParagraphFormat-Konfiguration erstellt.
// Der erste Absatz erhält keinen Seitenumbruch.
// Belassen Sie dieses Flag auf „false“, um jeden neuen Absatz auf derselben Seite zu beginnen
// wie zuvor, sofern ausreichend Platz vorhanden ist.
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

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../paragraphformat/)
* Montage [Aspose.Words](../../../)


