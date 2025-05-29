---
title: Font.Bold
linktitle: Bold
articleTitle: Bold
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font Bold, identifica facilmente se il tuo testo è in grassetto, migliorando la leggibilità e lo stile dei tuoi progetti di web design.
type: docs
weight: 40
url: /it/net/aspose.words/font/bold/
---
## Font.Bold property

Vero se il font è formattato in grassetto.

```csharp
public bool Bold { get; set; }
```

## Esempi

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
