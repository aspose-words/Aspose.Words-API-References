---
title: BorderCollection.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words per .NET
description: BorderCollection Shadow proprietà. Ottiene o imposta un valore che indica se il bordo ha unombra in C#.
type: docs
weight: 110
url: /it/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

Ottiene o imposta un valore che indica se il bordo ha un'ombra.

```csharp
public bool Shadow { get; set; }
```

## Osservazioni

Ottiene il valore dal primo bordo nella raccolta.

Imposta il valore per tutti i bordi nella raccolta esclusi i bordi diagonali.

## Esempi

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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
