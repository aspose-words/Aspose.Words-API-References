---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font Shadow e arricchisci il tuo testo con eleganti effetti ombra per conferire un impatto visivo sorprendente ai tuoi progetti.
type: docs
weight: 340
url: /it/net/aspose.words/font/shadow/
---
## Font.Shadow property

Vero se il font è formattato come ombreggiato.

```csharp
public bool Shadow { get; set; }
```

## Esempi

Mostra come creare una sequenza di testo formattata con un'ombra.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta il flag Ombra per applicare un effetto ombra offset,
// facendo sembrare che le lettere fluttuino sopra la pagina.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
