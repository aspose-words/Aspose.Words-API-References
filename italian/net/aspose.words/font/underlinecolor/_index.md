---
title: Font.UnderlineColor
linktitle: UnderlineColor
articleTitle: UnderlineColor
second_title: Aspose.Words per .NET
description: Font UnderlineColor proprietà. Ottiene o imposta il colore della sottolineatura applicata al carattere in C#.
type: docs
weight: 540
url: /it/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

Ottiene o imposta il colore della sottolineatura applicata al carattere.

```csharp
public Color UnderlineColor { get; set; }
```

## Esempi

Mostra come configurare lo stile e il colore della sottolineatura del testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
