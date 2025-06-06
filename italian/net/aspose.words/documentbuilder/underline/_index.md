---
title: DocumentBuilder.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words per .NET
description: Scopri la proprietà "Sottolineato" di DocumentBuilder per personalizzare facilmente gli stili dei font. Migliora i tuoi documenti con versatili opzioni di sottolineatura per un aspetto professionale.
type: docs
weight: 190
url: /it/net/aspose.words/documentbuilder/underline/
---
## DocumentBuilder.Underline property

Ottiene/imposta il tipo di sottolineatura per il font corrente.

```csharp
public Underline Underline { get; set; }
```

## Esempi

Mostra come formattare il testo inserito da un generatore di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Dash;
builder.Font.Color = Color.Blue;
builder.Font.Size = 32;

// Il builder applica la formattazione al paragrafo corrente e a qualsiasi nuovo testo aggiunto in seguito.
builder.Writeln("Large, blue, and underlined text.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### Guarda anche

* enum [Underline](../../underline/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
