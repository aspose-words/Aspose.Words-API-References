---
title: Border.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words per .NET
description: Border LineStyle proprietà. Ottiene o imposta lo stile del bordo in C#.
type: docs
weight: 40
url: /it/net/aspose.words/border/linestyle/
---
## Border.LineStyle property

Ottiene o imposta lo stile del bordo.

```csharp
public LineStyle LineStyle { get; set; }
```

## Osservazioni

Se imposti lo stile della linea su nessuno, la larghezza della linea verrà automaticamente modificata su zero.

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

* enum [LineStyle](../../linestyle/)
* class [Border](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
