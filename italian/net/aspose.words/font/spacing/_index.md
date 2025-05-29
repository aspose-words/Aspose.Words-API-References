---
title: Font.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words per .NET
description: Scopri la proprietà "Spaziatura caratteri" per regolare facilmente la spaziatura dei caratteri in punti. Migliora la leggibilità e il design con un controllo tipografico preciso.
type: docs
weight: 390
url: /it/net/aspose.words/font/spacing/
---
## Font.Spacing property

Restituisce o imposta la spaziatura (in punti) tra i caratteri .

```csharp
public double Spacing { get; set; }
```

## Esempi

Mostra come impostare il ridimensionamento orizzontale e la spaziatura per i caratteri.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiungere una sequenza di testo e aumentare la larghezza del carattere al 150%.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Aggiungere una sequenza di testo e aggiungere 1 pt di spaziatura orizzontale extra tra ogni carattere.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Aggiunge una sequenza di testo e avvicina i caratteri di 1 pt.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
