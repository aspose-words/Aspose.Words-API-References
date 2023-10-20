---
title: Border.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words per .NET
description: Border Color proprietà. Ottiene o imposta il colore del bordo in C#.
type: docs
weight: 10
url: /it/net/aspose.words/border/color/
---
## Border.Color property

Ottiene o imposta il colore del bordo.

```csharp
public Color Color { get; set; }
```

## Esempi

Mostra come inserire una stringa circondata da un bordo in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### Guarda anche

* class [Border](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
