---
title: Font.Outline
linktitle: Outline
articleTitle: Outline
second_title: Aspose.Words per .NET
description: Scopri la proprietà Contorno Font. Formatta facilmente i font come contorni per un tocco di design unico. Migliora la tua tipografia con questa semplice funzionalità!
type: docs
weight: 300
url: /it/net/aspose.words/font/outline/
---
## Font.Outline property

Vero se il font è formattato come contorno.

```csharp
public bool Outline { get; set; }
```

## Esempi

Mostra come creare una sequenza di testo formattata come struttura.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta il flag Outline per cambiare il colore di riempimento del testo in bianco e
 // lascia un sottile contorno attorno a ciascun carattere nel colore originale del testo.
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
