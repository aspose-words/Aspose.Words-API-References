---
title: BorderCollection.Color
second_title: Aspose.Words per .NET API Reference
description: BorderCollection proprietà. Ottiene o imposta il colore del bordo.
type: docs
weight: 20
url: /it/net/aspose.words/bordercollection/color/
---
## BorderCollection.Color property

Ottiene o imposta il colore del bordo.

```csharp
public Color Color { get; set; }
```

### Osservazioni

Restituisce il colore del primo bordo della raccolta.

Imposta il colore di tutti i bordi della raccolta esclusi i bordi diagonali.

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

* class [BorderCollection](../)
* spazio dei nomi [Aspose.Words](../../bordercollection/)
* assemblea [Aspose.Words](../../../)


