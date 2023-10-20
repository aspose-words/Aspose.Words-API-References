---
title: Font.HighlightColor
linktitle: HighlightColor
articleTitle: HighlightColor
second_title: Aspose.Words per .NET
description: Font HighlightColor proprietà. Ottiene o imposta il colore dellevidenziazione marcatore in C#.
type: docs
weight: 150
url: /it/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Ottiene o imposta il colore dell'evidenziazione (marcatore).

```csharp
public Color HighlightColor { get; set; }
```

## Esempi

Mostra come formattare una sequenza di testo utilizzando la relativa proprietà font.

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

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
