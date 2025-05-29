---
title: Font.EmphasisMark
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words per .NET
description: Scopri come utilizzare la proprietà "Segno di enfasi" per migliorare la formattazione del testo. Impara a impostare e personalizzare i segni di enfasi per una migliore leggibilità.
type: docs
weight: 110
url: /it/net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

Ottiene o imposta il segno di enfasi applicato a questa formattazione.

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

## Esempi

Mostra come aggiungere un carattere aggiuntivo visualizzato sopra/sotto il carattere glifo.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Possibili tipi di segno di enfasi:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### Guarda anche

* enum [EmphasisMark](../../emphasismark/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
