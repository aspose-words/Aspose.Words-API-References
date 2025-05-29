---
title: Paragraph.ParentSection
linktitle: ParentSection
articleTitle: ParentSection
second_title: Aspose.Words per .NET
description: Scopri la proprietà Paragraph ParentSection per accedere facilmente alla sezione padre di qualsiasi paragrafo, migliorando così la struttura e l'organizzazione del tuo documento.
type: docs
weight: 200
url: /it/net/aspose.words/paragraph/parentsection/
---
## Paragraph.ParentSection property

Recupera il genitore[`Section`](../../section/) del paragrafo.

```csharp
public Section ParentSection { get; }
```

## Esempi

Mostra come creare un'intestazione e un piè di pagina.

```csharp
Document doc = new Document();

// Crea un'intestazione e aggiungi un paragrafo. Il testo in quel paragrafo
// apparirà in cima a ogni pagina di questa sezione, sopra il testo principale.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Crea un piè di pagina e aggiungi un paragrafo. Il testo in quel paragrafo
// apparirà in fondo a ogni pagina di questa sezione, sotto il testo principale.
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

### Guarda anche

* class [Section](../../section/)
* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
