---
title: Paragraph.BreakIsStyleSeparator
linktitle: BreakIsStyleSeparator
articleTitle: BreakIsStyleSeparator
second_title: Aspose.Words per .NET
description: Scopri come la proprietà Paragraph Break IsStyleSeparator migliora la formattazione del documento consentendo stili di paragrafo misti per una maggiore flessibilità di progettazione.
type: docs
weight: 20
url: /it/net/aspose.words/paragraph/breakisstyleseparator/
---
## Paragraph.BreakIsStyleSeparator property

Vero se questa interruzione di paragrafo è un separatore di stile. Un separatore di stile consente a un paragrafo di essere composto da parti con stili di paragrafo diversi.

```csharp
public bool BreakIsStyleSeparator { get; }
```

## Esempi

Mostra come scrivere del testo sulla stessa riga di un titolo di indice senza che venga visualizzato nell'indice.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertTableOfContents("\\o \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Inserisci un paragrafo con uno stile che l'indice rileverà come voce.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

// Entrambe queste stringhe si trovano nello stesso paragrafo e pertanto verranno visualizzate nella stessa voce dell'indice.
builder.Write("Heading 1. ");
builder.Write("Will appear in the TOC. ");

// Se inseriamo un separatore di stile, possiamo scrivere più testo nello stesso paragrafo
// e utilizzare uno stile diverso senza comparire nell'indice.
// Se utilizziamo uno stile di tipo titolo dopo il separatore, possiamo trarre più voci di indice da una riga di testo del documento.
builder.InsertStyleSeparator();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Quote;
builder.Write("Won't appear in the TOC. ");

Assert.True(doc.FirstSection.Body.FirstParagraph.BreakIsStyleSeparator);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Paragraph.BreakIsStyleSeparator.docx");
```

### Guarda anche

* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
