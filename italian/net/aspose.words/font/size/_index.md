---
title: Font.Size
linktitle: Size
articleTitle: Size
second_title: Aspose.Words per .NET
description: Regola facilmente la dimensione del carattere con la proprietà "Dimensione carattere". Personalizza il tuo testo in punti per una migliore leggibilità e un design accattivante.
type: docs
weight: 350
url: /it/net/aspose.words/font/size/
---
## Font.Size property

Ottiene o imposta la dimensione del carattere in punti.

```csharp
public double Size { get; set; }
```

## Esempi

Mostra come formattare una sequenza di testo utilizzando la proprietà font.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Mostra come inserire testo formattato utilizzando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specificare la formattazione del carattere, quindi aggiungere il testo.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
