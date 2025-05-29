---
title: Font.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font Italic! Formatta facilmente il testo in corsivo per migliorare la leggibilità e lo stile dei tuoi progetti. Migliora la tua tipografia oggi stesso!
type: docs
weight: 160
url: /it/net/aspose.words/font/italic/
---
## Font.Italic property

Vero se il font è formattato in corsivo.

```csharp
public bool Italic { get; set; }
```

## Esempi

Mostra come scrivere testo in corsivo utilizzando uno strumento di creazione di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Italic = true;
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "Font.Italic.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
