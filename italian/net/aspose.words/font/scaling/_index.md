---
title: Font.Scaling
linktitle: Scaling
articleTitle: Scaling
second_title: Aspose.Words per .NET
description: Font Scaling proprietà. Ottiene o imposta il ridimensionamento della larghezza dei caratteri in percentuale in C#.
type: docs
weight: 310
url: /it/net/aspose.words/font/scaling/
---
## Font.Scaling property

Ottiene o imposta il ridimensionamento della larghezza dei caratteri in percentuale.

```csharp
public int Scaling { get; set; }
```

## Esempi

Mostra come impostare il ridimensionamento e la spaziatura orizzontale per i caratteri.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiunge una sequenza di testo e aumenta la larghezza del carattere al 150%.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Aggiunge una sequenza di testo e aggiunge 1 punto di spaziatura orizzontale extra tra ogni carattere.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Aggiungi sequenza di testo e avvicina i caratteri di 1 pt.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
