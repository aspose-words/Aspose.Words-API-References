---
title: Font.Outline
linktitle: Outline
articleTitle: Outline
second_title: Aspose.Words per .NET
description: Font Outline proprietà. Vero se il carattere è formattato come contorno in C#.
type: docs
weight: 290
url: /it/net/aspose.words/font/outline/
---
## Font.Outline property

Vero se il carattere è formattato come contorno.

```csharp
public bool Outline { get; set; }
```

## Esempi

Mostra come creare una sequenza di testo formattata come contorno.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta il flag Contorno per cambiare il colore di riempimento del testo in bianco e
 // lascia un contorno sottile attorno a ciascun carattere nel colore originale del testo.
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
