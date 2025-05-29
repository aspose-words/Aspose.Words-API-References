---
title: Font.Kerning
linktitle: Kerning
articleTitle: Kerning
second_title: Aspose.Words per .NET
description: Scopri la proprietà "Font Kerning" e controlla quando applicare la crenatura per una chiarezza e un design ottimali del testo. Migliora la tua tipografia con precisione!
type: docs
weight: 180
url: /it/net/aspose.words/font/kerning/
---
## Font.Kerning property

Ottiene o imposta la dimensione del carattere da cui inizia la crenatura.

```csharp
public double Kerning { get; set; }
```

## Esempi

Mostra come specificare la dimensione del carattere a partire dalla quale la crenatura inizia a diventare effettiva.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// Imposta la dimensione del carattere del builder e la dimensione minima alla quale avrà effetto la crenatura.
// La dimensione del carattere è al di sotto della soglia di kerning, quindi la parte seguente non avrà kerning.
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// Imposta la soglia di crenatura in modo che la dimensione del carattere corrente del builder sia superiore a tale soglia.
// A qualsiasi testo che aggiungiamo da questo punto verrà applicata la crenatura. Gli spazi tra i caratteri
// verrà modificato, producendo normalmente un testo esteticamente leggermente più gradevole.
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
