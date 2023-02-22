---
title: Border.LineWidth
second_title: Aspose.Words per .NET API Reference
description: Border proprietà. Ottiene o imposta la larghezza del bordo in punti.
type: docs
weight: 50
url: /it/net/aspose.words/border/linewidth/
---
## Border.LineWidth property

Ottiene o imposta la larghezza del bordo in punti.

```csharp
public double LineWidth { get; set; }
```

### Osservazioni

Se si imposta una larghezza della linea maggiore di zero quando lo stile della linea è nessuno, lo stile della linea viene automaticamente modificato in linea singola.

### Esempi

Mostra come inserire una stringa racchiusa da un bordo in un documento.

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
* spazio dei nomi [Aspose.Words](../../border/)
* assemblea [Aspose.Words](../../../)


