---
title: Font.Outline
second_title: Aspose.Words per .NET API Reference
description: Font proprietà. Vero se il carattere è formattato come contorno.
type: docs
weight: 290
url: /it/net/aspose.words/font/outline/
---
## Font.Outline property

Vero se il carattere è formattato come contorno.

```csharp
public bool Outline { get; set; }
```

### Esempi

Mostra come creare una sequenza di testo formattato come struttura.

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
* spazio dei nomi [Aspose.Words](../../font/)
* assemblea [Aspose.Words](../../../)


