---
title: Font.TextEffect
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font TextEffect per personalizzare facilmente le animazioni dei font, migliorando i tuoi progetti con effetti di testo dinamici per un'esperienza utente accattivante.
type: docs
weight: 460
url: /it/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

Ottiene o imposta l'effetto di animazione del font.

```csharp
public TextEffect TextEffect { get; set; }
```

## Esempi

Mostra come applicare un effetto visivo a una corsa.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Le versioni precedenti di Microsoft Word supportano solo gli effetti di animazione dei caratteri.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Guarda anche

* enum [TextEffect](../../texteffect/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
