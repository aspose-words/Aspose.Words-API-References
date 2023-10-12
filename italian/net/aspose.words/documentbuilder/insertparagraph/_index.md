---
title: DocumentBuilder.InsertParagraph
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Inserisce uninterruzione di paragrafo nel documento.
type: docs
weight: 430
url: /it/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

Inserisce un'interruzione di paragrafo nel documento.

```csharp
public Paragraph InsertParagraph()
```

### Valore di ritorno

Il nodo del paragrafo appena inserito. È lo stesso nodo di[`CurrentParagraph`](../currentparagraph/).

### Osservazioni

Formattazione del paragrafo corrente specificata da[`ParagraphFormat`](../paragraphformat/) la proprietà viene utilizzata.

Spezza il paragrafo corrente in due. Dopo aver inserito il paragrafo, il cursore viene posizionato all'inizio del nuovo paragrafo.

Viene generata un'eccezione se non è possibile inserire un'interruzione di paragrafo nella posizione corrente del cursore.

### Esempi

Mostra come inserire un paragrafo nel documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Arial";
font.Underline = Underline.Dash;

ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.FirstLineIndent = 8;
paragraphFormat.Alignment = ParagraphAlignment.Justify;
paragraphFormat.AddSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.AddSpaceBetweenFarEastAndDigit = true;
paragraphFormat.KeepTogether = true;

// Il metodo "Writeln" termina il paragrafo dopo aver aggiunto il testo
// e poi inizia una nuova riga, aggiungendo un nuovo paragrafo.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Guarda anche

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


