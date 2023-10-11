---
title: Border.Shadow
second_title: Aspose.Words per .NET API Reference
description: Border proprietà. Ottiene o imposta un valore che indica se il bordo ha unombra.
type: docs
weight: 60
url: /it/net/aspose.words/border/shadow/
---
## Border.Shadow property

Ottiene o imposta un valore che indica se il bordo ha un'ombra.

```csharp
public bool Shadow { get; set; }
```

### Osservazioni

In Microsoft Word, affinché un bordo abbia un'ombra, i bordi su tutti e quattro i lati (sinistro, superiore, destro e inferiore) dovrebbero essere dello stesso tipo, larghezza, colore e tutti dovrebbero avere la proprietà Ombra impostata su`VERO`.

### Esempi

Mostra come creare un bordo verde ondulato della pagina con un'ombra.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### Guarda anche

* class [Border](../)
* spazio dei nomi [Aspose.Words](../../border/)
* assemblea [Aspose.Words](../../../)


