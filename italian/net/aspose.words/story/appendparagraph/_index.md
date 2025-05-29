---
title: Story.AppendParagraph
linktitle: AppendParagraph
articleTitle: AppendParagraph
second_title: Aspose.Words per .NET
description: Scopri il metodo Story AppendParagraph, crea e aggiungi senza sforzo un oggetto Paragrafo con testo personalizzabile per un miglioramento fluido del documento.
type: docs
weight: 60
url: /it/net/aspose.words/story/appendparagraph/
---
## Story.AppendParagraph method

Un metodo di scelta rapida che crea un[`Paragraph`](../../paragraph/) oggetto con testo facoltativo e lo aggiunge alla fine di questo oggetto.

```csharp
public Paragraph AppendParagraph(string text)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| text | String | Il testo del paragrafo. Può essere`null` o stringa vuota. |

### Valore di ritorno

Il paragrafo appena creato e aggiunto.

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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
