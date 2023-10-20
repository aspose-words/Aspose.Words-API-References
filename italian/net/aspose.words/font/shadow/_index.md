---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words per .NET
description: Font Shadow proprietà. Vero se il carattere è formattato come ombreggiato in C#.
type: docs
weight: 330
url: /it/net/aspose.words/font/shadow/
---
## Font.Shadow property

Vero se il carattere è formattato come ombreggiato.

```csharp
public bool Shadow { get; set; }
```

## Esempi

Mostra come creare una sequenza di testo formattata con un'ombra.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta il flag Shadow per applicare un effetto ombra offset,
// facendo sembrare che le lettere fluttuano sopra la pagina.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
