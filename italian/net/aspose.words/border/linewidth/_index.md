---
title: Border.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words per .NET
description: Regola la proprietà Border LineWidth per personalizzare lo spessore del bordo in punti, migliorando così la precisione e l'aspetto visivo del tuo progetto.
type: docs
weight: 50
url: /it/net/aspose.words/border/linewidth/
---
## Border.LineWidth property

Ottiene o imposta la larghezza del bordo in punti.

```csharp
public double LineWidth { get; set; }
```

## Osservazioni

Se si imposta una larghezza della linea maggiore di zero quando lo stile della linea è impostato su "nessuno", lo stile della linea is viene automaticamente modificato in linea singola.

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
