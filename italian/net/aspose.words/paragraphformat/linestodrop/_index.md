---
title: ParagraphFormat.LinesToDrop
linktitle: LinesToDrop
articleTitle: LinesToDrop
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ParagraphFormat LinesToDrop migliora l'altezza dei capilettera nei tuoi documenti. Ottimizza il layout del testo per ottenere immagini straordinarie!
type: docs
weight: 210
url: /it/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

Ottiene o imposta il numero di righe del testo del paragrafo utilizzato per calcolare l'altezza del capolettera.

```csharp
public int LinesToDrop { get; set; }
```

## Esempi

Mostra come impostare la dimensione di un capolettera.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifica la proprietà "LinesToDrop" per designare un paragrafo come capolettera,
// che lo trasformerà in una grande lettera maiuscola che decorerà il paragrafo successivo.
// Assegna a questa proprietà il valore 4 per dare al capolettera un'altezza pari a quattro righe di testo.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// Reimposta la proprietà "LinesToDrop" su 0 per trasformare il paragrafo successivo in un paragrafo normale.
// Il testo in questo paragrafo verrà disposto attorno al capolettera.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
