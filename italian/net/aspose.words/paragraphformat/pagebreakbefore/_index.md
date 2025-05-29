---
title: ParagraphFormat.PageBreakBefore
linktitle: PageBreakBefore
articleTitle: PageBreakBefore
second_title: Aspose.Words per .NET
description: Scopri la proprietà ParagraphFormat PageBreakBefore e controlla facilmente le interruzioni di pagina prima dei paragrafi per migliorare la formattazione e la leggibilità del documento.
type: docs
weight: 270
url: /it/net/aspose.words/paragraphformat/pagebreakbefore/
---
## ParagraphFormat.PageBreakBefore property

Vero se un'interruzione di pagina viene forzata prima del paragrafo.

```csharp
public bool PageBreakBefore { get; set; }
```

## Esempi

Mostra come creare paragrafi con interruzioni di pagina all'inizio.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta questo flag su "true" per applicare un'interruzione di pagina all'inizio di ogni paragrafo
// che il generatore di documenti creerà con questa configurazione ParagraphFormat.
// Il primo paragrafo non avrà un'interruzione di pagina.
// Lascia questo flag su "false" per iniziare ogni nuovo paragrafo sulla stessa pagina
// come il precedente, a patto che ci sia spazio sufficiente.
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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
