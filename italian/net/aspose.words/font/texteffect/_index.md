---
title: Font.TextEffect
second_title: Aspose.Words per .NET API Reference
description: Font proprietà. Ottiene o imposta leffetto di animazione del carattere.
type: docs
weight: 450
url: /it/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

Ottiene o imposta l'effetto di animazione del carattere.

```csharp
public TextEffect TextEffect { get; set; }
```

### Esempi

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
* spazio dei nomi [Aspose.Words](../../font/)
* assemblea [Aspose.Words](../../../)


