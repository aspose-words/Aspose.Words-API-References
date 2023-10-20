---
title: PageSetup.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words per .NET
description: PageSetup Borders proprietà. Ottiene una raccolta dei bordi della pagina in C#.
type: docs
weight: 50
url: /it/net/aspose.words/pagesetup/borders/
---
## PageSetup.Borders property

Ottiene una raccolta dei bordi della pagina.

```csharp
public BorderCollection Borders { get; }
```

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

* class [BorderCollection](../../bordercollection/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
