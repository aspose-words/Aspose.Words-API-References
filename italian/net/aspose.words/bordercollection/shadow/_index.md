---
title: BorderCollection.Shadow
second_title: Aspose.Words per .NET API Reference
description: BorderCollection proprietà. Ottiene o imposta un valore che indica se il bordo ha unombra.
type: docs
weight: 110
url: /it/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

Ottiene o imposta un valore che indica se il bordo ha un'ombra.

```csharp
public bool Shadow { get; set; }
```

### Osservazioni

Ottiene il valore dal primo bordo della raccolta.

Imposta il valore per tutti i bordi nella raccolta esclusi i bordi diagonali.

### Esempi

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
* spazio dei nomi [Aspose.Words](../../bordercollection/)
* assemblea [Aspose.Words](../../../)


