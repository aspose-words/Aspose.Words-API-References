---
title: Paragraph.BreakIsStyleSeparator
second_title: Aspose.Words per .NET API Reference
description: Paragraph proprietà. Vero se questa interruzione di paragrafo è un separatore di stile. Un separatore di stile consente a un paragrafo di essere costituito da parti con stili di paragrafo diversi.
type: docs
weight: 20
url: /it/net/aspose.words/paragraph/breakisstyleseparator/
---
## Paragraph.BreakIsStyleSeparator property

Vero se questa interruzione di paragrafo è un separatore di stile. Un separatore di stile consente a un paragrafo di essere costituito da parti con stili di paragrafo diversi.

```csharp
public bool BreakIsStyleSeparator { get; }
```

### Esempi

Mostra come scrivere il testo sulla stessa riga dell'intestazione del sommario e non visualizzarlo nel sommario.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertTableOfContents("\\o \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Inserisci un paragrafo con uno stile che il sommario prenderà come voce.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

// Entrambe queste stringhe si trovano nello stesso paragrafo e pertanto verranno visualizzate nella stessa voce del sommario.
builder.Write("Heading 1. ");
builder.Write("Will appear in the TOC. ");

// Se inseriamo un separatore di stile, possiamo scrivere più testo nello stesso paragrafo
// e utilizza uno stile diverso senza essere visualizzato nel sommario.
// Se usiamo uno stile di tipo intestazione dopo il separatore, possiamo disegnare più voci di sommario da una riga di testo del documento.
builder.InsertStyleSeparator();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Quote;
builder.Write("Won't appear in the TOC. ");

Assert.True(doc.FirstSection.Body.FirstParagraph.BreakIsStyleSeparator);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Paragraph.BreakIsStyleSeparator.docx");
```

### Guarda anche

* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../paragraph/)
* assemblea [Aspose.Words](../../../)


