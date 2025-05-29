---
title: BorderCollection.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words per .NET
description: Scopri la proprietà BorderCollection DistanceFromText per personalizzare facilmente la spaziatura dei bordi rispetto al testo nei tuoi progetti. Ottimizza il tuo layout senza sforzo!
type: docs
weight: 40
url: /it/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

Ottiene o imposta la distanza del bordo dal testo in punti.

```csharp
public double DistanceFromText { get; set; }
```

## Osservazioni

Ottiene la distanza dal testo per il primo bordo.

Imposta la distanza dal testo per tutti i bordi della raccolta, esclusi i bordi diagonali.

Non ha alcun effetto e verrà automaticamente reimpostato a zero per i bordi delle celle della tabella.

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
