---
title: BorderCollection.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words per .NET
description: Scopri la proprietà BorderCollection LineStyle per personalizzare il tuo design con stili di bordo flessibili. Migliora l'aspetto visivo del tuo progetto senza sforzo!
type: docs
weight: 80
url: /it/net/aspose.words/bordercollection/linestyle/
---
## BorderCollection.LineStyle property

Ottiene o imposta lo stile del bordo.

```csharp
public LineStyle LineStyle { get; set; }
```

## Osservazioni

Restituisce lo stile del primo bordo nella raccolta.

Imposta lo stile di tutti i bordi nella raccolta, esclusi i bordi diagonali.

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

* enum [LineStyle](../../linestyle/)
* class [BorderCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
