---
title: BorderCollection.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words per .NET
description: Scopri la proprietà BorderCollection LineWidth per regolare facilmente la larghezza del bordo in punti, migliorando la precisione e l'attrattiva visiva del tuo design.
type: docs
weight: 90
url: /it/net/aspose.words/bordercollection/linewidth/
---
## BorderCollection.LineWidth property

Ottiene o imposta la larghezza del bordo in punti.

```csharp
public double LineWidth { get; set; }
```

## Osservazioni

Restituisce la larghezza del primo bordo nella raccolta.

Imposta la larghezza di tutti i bordi nella raccolta, esclusi i bordi diagonali.

## Esempi

Mostra come creare un bordo di pagina ondulato verde con un'ombra.

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

* class [BorderCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
