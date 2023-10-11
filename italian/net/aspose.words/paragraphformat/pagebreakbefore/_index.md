---
title: ParagraphFormat.PageBreakBefore
second_title: Aspose.Words per .NET API Reference
description: ParagraphFormat proprietà. Vero se viene forzata uninterruzione di pagina prima del paragrafo.
type: docs
weight: 260
url: /it/net/aspose.words/paragraphformat/pagebreakbefore/
---
## ParagraphFormat.PageBreakBefore property

Vero se viene forzata un'interruzione di pagina prima del paragrafo.

```csharp
public bool PageBreakBefore { get; set; }
```

### Esempi

Mostra come creare paragrafi con interruzioni di pagina all'inizio.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta questo flag su "true" per applicare un'interruzione di pagina all'inizio di ogni paragrafo
// che il generatore di documenti creerà in questa configurazione ParagraphFormat.
// Il primo paragrafo non riceverà un'interruzione di pagina.
// Lascia questo flag su "false" per iniziare ogni nuovo paragrafo sulla stessa pagina
// come il precedente, purché ci sia spazio sufficiente.
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

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../paragraphformat/)
* assemblea [Aspose.Words](../../../)


