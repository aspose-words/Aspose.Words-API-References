---
title: Font.NoProofing
second_title: Aspose.Words per .NET API Reference
description: Font proprietà. Vero quando i caratteri formattati non devono essere sottoposti al controllo ortografico.
type: docs
weight: 280
url: /it/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

Vero quando i caratteri formattati non devono essere sottoposti al controllo ortografico.

```csharp
public bool NoProofing { get; set; }
```

### Esempi

Mostra come impedire il controllo ortografico del testo da parte di Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Normalmente, Microsoft Word evidenzia gli errori di ortografia con una sottolineatura rossa frastagliata.
// Possiamo deselezionare il flag "NoProofing" per creare una porzione di testo that
// ignora il controllo ortografico disabilitandolo completamente.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../font/)
* assemblea [Aspose.Words](../../../)


