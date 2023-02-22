---
title: ParagraphFormat.KeepTogether
second_title: Aspose.Words per .NET API Reference
description: ParagraphFormat proprietà. Vero se tutte le righe del paragrafo devono rimanere sulla stessa pagina.
type: docs
weight: 150
url: /it/net/aspose.words/paragraphformat/keeptogether/
---
## ParagraphFormat.KeepTogether property

Vero se tutte le righe del paragrafo devono rimanere sulla stessa pagina.

```csharp
public bool KeepTogether { get; set; }
```

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
// e quindi inizia una nuova riga, aggiungendo un nuovo paragrafo.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../paragraphformat/)
* assemblea [Aspose.Words](../../../)


