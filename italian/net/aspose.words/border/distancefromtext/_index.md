---
title: Border.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words per .NET
description: Border DistanceFromText proprietà. Ottiene o imposta la distanza del bordo dal testo o dal bordo della pagina in punti in C#.
type: docs
weight: 20
url: /it/net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

Ottiene o imposta la distanza del bordo dal testo o dal bordo della pagina in punti.

```csharp
public double DistanceFromText { get; set; }
```

## Osservazioni

Non ha alcun effetto e verrà automaticamente reimpostato su zero per i bordi delle celle della tabella.

## Esempi

Mostra come creare un ampio bordo a fascia blu nella parte superiore della prima pagina.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
```

### Guarda anche

* class [Border](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
