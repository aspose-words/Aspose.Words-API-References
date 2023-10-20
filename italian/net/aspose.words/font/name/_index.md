---
title: Font.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words per .NET
description: Font Name proprietà. Ottiene o imposta il nome del carattere in C#.
type: docs
weight: 230
url: /it/net/aspose.words/font/name/
---
## Font.Name property

Ottiene o imposta il nome del carattere.

```csharp
public string Name { get; set; }
```

## Osservazioni

Quando si ottiene, ritorna[`NameAscii`](../nameascii/).

Quando si imposta, imposta[`NameAscii`](../nameascii/) ,[`NameBi`](../namebi/) ,[`NameFarEast`](../namefareast/) e[`NameOther`](../nameother/) al valore specificato.

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

Mostra come inserire testo formattato utilizzando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specifica la formattazione del carattere, quindi aggiunge il testo.
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
