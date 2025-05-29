---
title: Border.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words per .NET
description: Personalizza il tuo design con la proprietà Border LineStyle, che ti consente di ottenere o impostare facilmente stili di bordo unici per un impatto visivo migliore.
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

Se si imposta lo stile della linea su "Nessuno", la larghezza della linea verrà automaticamente impostata su zero.

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
